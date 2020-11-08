---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047477"
---
# <span data-ttu-id="bb6e3-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="bb6e3-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="bb6e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb6e3-102">SYNOPSIS</span></span>
<span data-ttu-id="bb6e3-103">지정 된 외부 서비스 이벤트에 대 한 이벤트 트리거의 구독 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bb6e3-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="bb6e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb6e3-104">SYNTAX</span></span>

### <span data-ttu-id="bb6e3-105">GetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="bb6e3-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb6e3-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="bb6e3-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb6e3-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="bb6e3-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb6e3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bb6e3-108">DESCRIPTION</span></span>
<span data-ttu-id="bb6e3-109">**AzSynapseTriggerSubscriptionStatus** cmdlet은 지정 된 외부 서비스 이벤트에 대 한 이벤트 트리거의 구독 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bb6e3-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="bb6e3-110">반환 된 상태가 "사용"이 될 때까지 트리거를 시작할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bb6e3-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="bb6e3-111">예제의</span><span class="sxs-lookup"><span data-stu-id="bb6e3-111">EXAMPLES</span></span>

### <span data-ttu-id="bb6e3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="bb6e3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="bb6e3-113">이 명령을 실행 하면 외부 서비스 이벤트에 대 한 ContosoTrigger 이라는 subscribtion의 상태가 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bb6e3-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="bb6e3-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="bb6e3-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="bb6e3-115">이 명령은 파이프라인을 통해 외부 서비스 이벤트에 대해 ContosoTrigger 라는 subscribtion 트리거의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bb6e3-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="bb6e3-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="bb6e3-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="bb6e3-117">이 명령은 파이프라인을 통해 외부 서비스 이벤트에 대해 ContosoTrigger 라는 subscribtion 트리거의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bb6e3-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="bb6e3-118">변수</span><span class="sxs-lookup"><span data-stu-id="bb6e3-118">PARAMETERS</span></span>

### <span data-ttu-id="bb6e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb6e3-119">-DefaultProfile</span></span>
<span data-ttu-id="bb6e3-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6e3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb6e3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb6e3-121">-InputObject</span></span>
<span data-ttu-id="bb6e3-122">트리거 개체</span><span class="sxs-lookup"><span data-stu-id="bb6e3-122">The trigger object.</span></span>

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

### <span data-ttu-id="bb6e3-123">-이름</span><span class="sxs-lookup"><span data-stu-id="bb6e3-123">-Name</span></span>
<span data-ttu-id="bb6e3-124">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6e3-124">The trigger name.</span></span>

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

### <span data-ttu-id="bb6e3-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bb6e3-125">-WorkspaceName</span></span>
<span data-ttu-id="bb6e3-126">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6e3-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bb6e3-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bb6e3-127">-WorkspaceObject</span></span>
<span data-ttu-id="bb6e3-128">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6e3-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bb6e3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb6e3-129">CommonParameters</span></span>
<span data-ttu-id="bb6e3-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6e3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb6e3-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bb6e3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb6e3-132">입력</span><span class="sxs-lookup"><span data-stu-id="bb6e3-132">INPUTS</span></span>

### <span data-ttu-id="bb6e3-133">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="bb6e3-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="bb6e3-134">Synapse. PSTriggerResource/.</span><span class="sxs-lookup"><span data-stu-id="bb6e3-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="bb6e3-135">출력</span><span class="sxs-lookup"><span data-stu-id="bb6e3-135">OUTPUTS</span></span>

### <span data-ttu-id="bb6e3-136">Synapse. PSTriggerSubscriptionOperationStatus/.</span><span class="sxs-lookup"><span data-stu-id="bb6e3-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="bb6e3-137">상속자</span><span class="sxs-lookup"><span data-stu-id="bb6e3-137">NOTES</span></span>

## <span data-ttu-id="bb6e3-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb6e3-138">RELATED LINKS</span></span>
