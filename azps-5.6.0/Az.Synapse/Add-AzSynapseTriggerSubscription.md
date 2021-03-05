---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: d9ff2e46b7b4ccf7b3d2fafd1aa8142efd0675b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981376"
---
# <span data-ttu-id="18eb4-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="18eb4-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="18eb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="18eb4-103">외부 서비스 이벤트에 이벤트 트리거를 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="18eb4-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="18eb4-104">구문</span><span class="sxs-lookup"><span data-stu-id="18eb4-104">SYNTAX</span></span>

### <span data-ttu-id="18eb4-105">AddByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="18eb4-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18eb4-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="18eb4-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18eb4-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="18eb4-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18eb4-108">설명</span><span class="sxs-lookup"><span data-stu-id="18eb4-108">DESCRIPTION</span></span>
<span data-ttu-id="18eb4-109">**Add-AzSynapseTriggerSubscription** cmdlet은 트리거 정의에서 지정된 외부 서비스 이벤트에 이벤트 트리거를 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="18eb4-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="18eb4-110">예제</span><span class="sxs-lookup"><span data-stu-id="18eb4-110">EXAMPLES</span></span>

### <span data-ttu-id="18eb4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="18eb4-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="18eb4-112">이 명령은 ContosoTrigger라는 트리거를 트리거 정의에서 지정된 이벤트에 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="18eb4-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="18eb4-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="18eb4-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="18eb4-114">이 명령은 트리거 정의부터 파이프라인까지 지정된 이벤트에 ContosoTrigger라는 트리거를 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="18eb4-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="18eb4-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="18eb4-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="18eb4-116">이 명령은 트리거 정의부터 파이프라인까지 지정된 이벤트에 ContosoTrigger라는 트리거를 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="18eb4-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="18eb4-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="18eb4-117">PARAMETERS</span></span>

### <span data-ttu-id="18eb4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18eb4-118">-AsJob</span></span>
<span data-ttu-id="18eb4-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="18eb4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18eb4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18eb4-120">-DefaultProfile</span></span>
<span data-ttu-id="18eb4-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18eb4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18eb4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18eb4-122">-InputObject</span></span>
<span data-ttu-id="18eb4-123">트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="18eb4-123">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: AddByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18eb4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="18eb4-124">-Name</span></span>
<span data-ttu-id="18eb4-125">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18eb4-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName, AddByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eb4-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="18eb4-126">-WorkspaceName</span></span>
<span data-ttu-id="18eb4-127">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18eb4-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eb4-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="18eb4-128">-WorkspaceObject</span></span>
<span data-ttu-id="18eb4-129">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="18eb4-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: AddByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18eb4-130">-확인</span><span class="sxs-lookup"><span data-stu-id="18eb4-130">-Confirm</span></span>
<span data-ttu-id="18eb4-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="18eb4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18eb4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18eb4-132">-WhatIf</span></span>
<span data-ttu-id="18eb4-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="18eb4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18eb4-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18eb4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18eb4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18eb4-135">CommonParameters</span></span>
<span data-ttu-id="18eb4-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="18eb4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18eb4-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18eb4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18eb4-138">입력</span><span class="sxs-lookup"><span data-stu-id="18eb4-138">INPUTS</span></span>

### <span data-ttu-id="18eb4-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="18eb4-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="18eb4-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="18eb4-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="18eb4-141">출력</span><span class="sxs-lookup"><span data-stu-id="18eb4-141">OUTPUTS</span></span>

### <span data-ttu-id="18eb4-142">System.Object</span><span class="sxs-lookup"><span data-stu-id="18eb4-142">System.Object</span></span>
## <span data-ttu-id="18eb4-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="18eb4-143">NOTES</span></span>

## <span data-ttu-id="18eb4-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18eb4-144">RELATED LINKS</span></span>
