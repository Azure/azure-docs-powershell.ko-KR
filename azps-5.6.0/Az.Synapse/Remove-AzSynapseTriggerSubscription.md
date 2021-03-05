---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: f331cad857fba20d72ffdd34f84f70a5d6392bff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002128"
---
# <span data-ttu-id="07db2-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="07db2-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="07db2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07db2-102">SYNOPSIS</span></span>
<span data-ttu-id="07db2-103">외부 서비스 이벤트에 대한 이벤트 트리거 구독을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="07db2-104">구문</span><span class="sxs-lookup"><span data-stu-id="07db2-104">SYNTAX</span></span>

### <span data-ttu-id="07db2-105">RemoveByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="07db2-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07db2-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="07db2-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07db2-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="07db2-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07db2-108">설명</span><span class="sxs-lookup"><span data-stu-id="07db2-108">DESCRIPTION</span></span>
<span data-ttu-id="07db2-109">**Remove-AzSynapseTriggerSubscription cmdlet은** 트리거 정의에서 지정된 외부 서비스 이벤트에 대한 이벤트 트리거를 구독 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="07db2-110">예제</span><span class="sxs-lookup"><span data-stu-id="07db2-110">EXAMPLES</span></span>

### <span data-ttu-id="07db2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="07db2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="07db2-112">이 명령은 ContosoTrigger라는 트리거를 트리거 정의에서 지정된 이벤트로 구독을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="07db2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="07db2-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="07db2-114">이 명령은 ContosoTrigger라는 트리거를 트리거 정의에서 파이프라인까지 지정된 이벤트로 구독을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="07db2-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="07db2-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="07db2-116">이 명령은 ContosoTrigger라는 트리거를 트리거 정의에서 파이프라인까지 지정된 이벤트로 구독을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="07db2-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="07db2-117">PARAMETERS</span></span>

### <span data-ttu-id="07db2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07db2-118">-AsJob</span></span>
<span data-ttu-id="07db2-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="07db2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07db2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07db2-120">-DefaultProfile</span></span>
<span data-ttu-id="07db2-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07db2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="07db2-122">-Force</span></span>
<span data-ttu-id="07db2-123">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="07db2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07db2-124">-InputObject</span></span>
<span data-ttu-id="07db2-125">트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-125">The trigger object.</span></span>

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

### <span data-ttu-id="07db2-126">-Name</span><span class="sxs-lookup"><span data-stu-id="07db2-126">-Name</span></span>
<span data-ttu-id="07db2-127">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-127">The trigger name.</span></span>

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

### <span data-ttu-id="07db2-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07db2-128">-PassThru</span></span>
<span data-ttu-id="07db2-129">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="07db2-130">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="07db2-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="07db2-131">-WorkspaceName</span></span>
<span data-ttu-id="07db2-132">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="07db2-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="07db2-133">-WorkspaceObject</span></span>
<span data-ttu-id="07db2-134">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="07db2-135">-확인</span><span class="sxs-lookup"><span data-stu-id="07db2-135">-Confirm</span></span>
<span data-ttu-id="07db2-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07db2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07db2-137">-WhatIf</span></span>
<span data-ttu-id="07db2-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07db2-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07db2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07db2-140">CommonParameters</span></span>
<span data-ttu-id="07db2-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07db2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07db2-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07db2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07db2-143">입력</span><span class="sxs-lookup"><span data-stu-id="07db2-143">INPUTS</span></span>

### <span data-ttu-id="07db2-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="07db2-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="07db2-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="07db2-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="07db2-146">출력</span><span class="sxs-lookup"><span data-stu-id="07db2-146">OUTPUTS</span></span>

### <span data-ttu-id="07db2-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="07db2-147">System.Boolean</span></span>

## <span data-ttu-id="07db2-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="07db2-148">NOTES</span></span>

## <span data-ttu-id="07db2-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07db2-149">RELATED LINKS</span></span>
