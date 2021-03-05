---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: c0c1b83f177b568e7058b973b788a633cfefe48c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970128"
---
# <span data-ttu-id="53293-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="53293-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="53293-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53293-102">SYNOPSIS</span></span>
<span data-ttu-id="53293-103">지정된 외부 서비스 이벤트에 대한 이벤트 트리거에 대한 구독 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="53293-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="53293-104">구문</span><span class="sxs-lookup"><span data-stu-id="53293-104">SYNTAX</span></span>

### <span data-ttu-id="53293-105">GetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="53293-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53293-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="53293-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53293-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="53293-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53293-108">설명</span><span class="sxs-lookup"><span data-stu-id="53293-108">DESCRIPTION</span></span>
<span data-ttu-id="53293-109">**Get-AzSynapseTriggerSubscriptionStatus** cmdlet은 지정된 외부 서비스 이벤트에 대한 이벤트 트리거에 대한 구독의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="53293-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="53293-110">반환된 상태가 "사용"으로 설정될 때까지 트리거를 시작할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="53293-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="53293-111">예제</span><span class="sxs-lookup"><span data-stu-id="53293-111">EXAMPLES</span></span>

### <span data-ttu-id="53293-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="53293-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="53293-113">이 명령은 ContosoTrigger라는 트리거에 대한 하위 구성의 상태를 외부 서비스 이벤트에 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="53293-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="53293-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="53293-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="53293-115">이 명령은 파이프라인을 통해 외부 서비스 이벤트에 ContosoTrigger라는 트리거에 대한 하위 구성 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="53293-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="53293-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="53293-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="53293-117">이 명령은 파이프라인을 통해 외부 서비스 이벤트에 ContosoTrigger라는 트리거에 대한 하위 구성 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="53293-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="53293-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="53293-118">PARAMETERS</span></span>

### <span data-ttu-id="53293-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53293-119">-DefaultProfile</span></span>
<span data-ttu-id="53293-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53293-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53293-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53293-121">-InputObject</span></span>
<span data-ttu-id="53293-122">트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="53293-122">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53293-123">-Name</span><span class="sxs-lookup"><span data-stu-id="53293-123">-Name</span></span>
<span data-ttu-id="53293-124">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53293-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, GetByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53293-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="53293-125">-WorkspaceName</span></span>
<span data-ttu-id="53293-126">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53293-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53293-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="53293-127">-WorkspaceObject</span></span>
<span data-ttu-id="53293-128">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="53293-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53293-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53293-129">CommonParameters</span></span>
<span data-ttu-id="53293-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="53293-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53293-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53293-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53293-132">입력</span><span class="sxs-lookup"><span data-stu-id="53293-132">INPUTS</span></span>

### <span data-ttu-id="53293-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="53293-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="53293-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="53293-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="53293-135">출력</span><span class="sxs-lookup"><span data-stu-id="53293-135">OUTPUTS</span></span>

### <span data-ttu-id="53293-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="53293-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="53293-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="53293-137">NOTES</span></span>

## <span data-ttu-id="53293-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53293-138">RELATED LINKS</span></span>
