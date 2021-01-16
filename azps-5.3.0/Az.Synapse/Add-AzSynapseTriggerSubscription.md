---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384168"
---
# <span data-ttu-id="d7de8-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="d7de8-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="d7de8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7de8-102">SYNOPSIS</span></span>
<span data-ttu-id="d7de8-103">이벤트 트리거를 외부 서비스 이벤트에 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="d7de8-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="d7de8-104">구문</span><span class="sxs-lookup"><span data-stu-id="d7de8-104">SYNTAX</span></span>

### <span data-ttu-id="d7de8-105">AddByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d7de8-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7de8-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="d7de8-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7de8-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="d7de8-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7de8-108">설명</span><span class="sxs-lookup"><span data-stu-id="d7de8-108">DESCRIPTION</span></span>
<span data-ttu-id="d7de8-109">**Add-AzSynapseTriggerSubscription** cmdlet은 트리거 정의에서 지정된 외부 서비스 이벤트에 이벤트 트리거를 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="d7de8-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="d7de8-110">예제</span><span class="sxs-lookup"><span data-stu-id="d7de8-110">EXAMPLES</span></span>

### <span data-ttu-id="d7de8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d7de8-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="d7de8-112">이 명령은 ContosoTrigger라는 트리거를 트리거 정의에서 지정된 이벤트로 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="d7de8-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="d7de8-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d7de8-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="d7de8-114">이 명령은 파이프라인을 통해 트리거 정의에서 지정된 이벤트에 ContosoTrigger라는 트리거를 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="d7de8-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="d7de8-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="d7de8-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="d7de8-116">이 명령은 파이프라인을 통해 트리거 정의에서 지정된 이벤트에 ContosoTrigger라는 트리거를 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="d7de8-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="d7de8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7de8-117">PARAMETERS</span></span>

### <span data-ttu-id="d7de8-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7de8-118">-AsJob</span></span>
<span data-ttu-id="d7de8-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d7de8-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7de8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7de8-120">-DefaultProfile</span></span>
<span data-ttu-id="d7de8-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7de8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7de8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7de8-122">-InputObject</span></span>
<span data-ttu-id="d7de8-123">트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d7de8-123">The trigger object.</span></span>

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

### <span data-ttu-id="d7de8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d7de8-124">-Name</span></span>
<span data-ttu-id="d7de8-125">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7de8-125">The trigger name.</span></span>

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

### <span data-ttu-id="d7de8-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d7de8-126">-WorkspaceName</span></span>
<span data-ttu-id="d7de8-127">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7de8-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d7de8-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d7de8-128">-WorkspaceObject</span></span>
<span data-ttu-id="d7de8-129">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d7de8-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d7de8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7de8-130">-Confirm</span></span>
<span data-ttu-id="d7de8-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7de8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7de8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7de8-132">-WhatIf</span></span>
<span data-ttu-id="d7de8-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d7de8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7de8-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7de8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7de8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7de8-135">CommonParameters</span></span>
<span data-ttu-id="d7de8-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d7de8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7de8-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d7de8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7de8-138">입력</span><span class="sxs-lookup"><span data-stu-id="d7de8-138">INPUTS</span></span>

### <span data-ttu-id="d7de8-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d7de8-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d7de8-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="d7de8-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="d7de8-141">출력</span><span class="sxs-lookup"><span data-stu-id="d7de8-141">OUTPUTS</span></span>

### <span data-ttu-id="d7de8-142">System.Object</span><span class="sxs-lookup"><span data-stu-id="d7de8-142">System.Object</span></span>
## <span data-ttu-id="d7de8-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d7de8-143">NOTES</span></span>

## <span data-ttu-id="d7de8-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7de8-144">RELATED LINKS</span></span>
