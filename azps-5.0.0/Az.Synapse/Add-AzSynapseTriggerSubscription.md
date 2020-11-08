---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217965"
---
# <span data-ttu-id="794d2-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="794d2-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="794d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="794d2-102">SYNOPSIS</span></span>
<span data-ttu-id="794d2-103">이벤트 트리거를 외부 서비스 이벤트에 가입 합니다.</span><span class="sxs-lookup"><span data-stu-id="794d2-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="794d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="794d2-104">SYNTAX</span></span>

### <span data-ttu-id="794d2-105">AddByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="794d2-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="794d2-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="794d2-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="794d2-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="794d2-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="794d2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="794d2-108">DESCRIPTION</span></span>
<span data-ttu-id="794d2-109">**Add-AzSynapseTriggerSubscription** cmdlet은 트리거 정의에서 지정 된 외부 서비스 이벤트에 대 한 이벤트 트리거를 구독 합니다.</span><span class="sxs-lookup"><span data-stu-id="794d2-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="794d2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="794d2-110">EXAMPLES</span></span>

### <span data-ttu-id="794d2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="794d2-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="794d2-112">이 명령은 트리거 정의에서 지정 된 이벤트에 ContosoTrigger 이라는 트리거를 구독 합니다.</span><span class="sxs-lookup"><span data-stu-id="794d2-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="794d2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="794d2-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="794d2-114">이 명령은 트리거 정의에서 파이프라인 까지의 지정 된 이벤트에 ContosoTrigger 이라는 트리거를 구독 합니다.</span><span class="sxs-lookup"><span data-stu-id="794d2-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="794d2-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="794d2-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="794d2-116">이 명령은 트리거 정의에서 파이프라인 까지의 지정 된 이벤트에 ContosoTrigger 이라는 트리거를 구독 합니다.</span><span class="sxs-lookup"><span data-stu-id="794d2-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="794d2-117">변수</span><span class="sxs-lookup"><span data-stu-id="794d2-117">PARAMETERS</span></span>

### <span data-ttu-id="794d2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="794d2-118">-AsJob</span></span>
<span data-ttu-id="794d2-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="794d2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="794d2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="794d2-120">-DefaultProfile</span></span>
<span data-ttu-id="794d2-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="794d2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="794d2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="794d2-122">-InputObject</span></span>
<span data-ttu-id="794d2-123">트리거 개체</span><span class="sxs-lookup"><span data-stu-id="794d2-123">The trigger object.</span></span>

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

### <span data-ttu-id="794d2-124">-이름</span><span class="sxs-lookup"><span data-stu-id="794d2-124">-Name</span></span>
<span data-ttu-id="794d2-125">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="794d2-125">The trigger name.</span></span>

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

### <span data-ttu-id="794d2-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="794d2-126">-WorkspaceName</span></span>
<span data-ttu-id="794d2-127">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="794d2-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="794d2-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="794d2-128">-WorkspaceObject</span></span>
<span data-ttu-id="794d2-129">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="794d2-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="794d2-130">-확인</span><span class="sxs-lookup"><span data-stu-id="794d2-130">-Confirm</span></span>
<span data-ttu-id="794d2-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="794d2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="794d2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="794d2-132">-WhatIf</span></span>
<span data-ttu-id="794d2-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="794d2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="794d2-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="794d2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="794d2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="794d2-135">CommonParameters</span></span>
<span data-ttu-id="794d2-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="794d2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="794d2-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="794d2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="794d2-138">입력</span><span class="sxs-lookup"><span data-stu-id="794d2-138">INPUTS</span></span>

### <span data-ttu-id="794d2-139">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="794d2-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="794d2-140">Synapse. PSTriggerResource/.</span><span class="sxs-lookup"><span data-stu-id="794d2-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="794d2-141">출력</span><span class="sxs-lookup"><span data-stu-id="794d2-141">OUTPUTS</span></span>

### <span data-ttu-id="794d2-142">System. 개체</span><span class="sxs-lookup"><span data-stu-id="794d2-142">System.Object</span></span>
## <span data-ttu-id="794d2-143">상속자</span><span class="sxs-lookup"><span data-stu-id="794d2-143">NOTES</span></span>

## <span data-ttu-id="794d2-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="794d2-144">RELATED LINKS</span></span>
