---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: 0f43535baa284dbe9f7c69aee5a688443172089a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000048"
---
# <span data-ttu-id="52718-101">Az.ResourceMover 모듈</span><span class="sxs-lookup"><span data-stu-id="52718-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="52718-102">설명</span><span class="sxs-lookup"><span data-stu-id="52718-102">Description</span></span>
<span data-ttu-id="52718-103">Microsoft Azure PowerShell: ResourceMover cmdlet</span><span class="sxs-lookup"><span data-stu-id="52718-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="52718-104">Az.ResourceMover Cmdlet</span><span class="sxs-lookup"><span data-stu-id="52718-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="52718-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="52718-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="52718-106">이동 컬렉션에서 리소스 이동을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="52718-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="52718-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="52718-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="52718-108">이동 컬렉션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52718-108">Gets the move collection.</span></span>

### [<span data-ttu-id="52718-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="52718-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="52718-110">리소스 이동을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52718-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="52718-111">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="52718-111">Get-AzResourceMoverRequiredForResources</span></span>](Get-AzResourceMoverRequiredForResources.md)
<span data-ttu-id="52718-112">팔 리소스가 필요한 이동 리소스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="52718-112">List of the move resources for which an arm resource is required for.</span></span>

### [<span data-ttu-id="52718-113">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="52718-113">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="52718-114">해결되지 않은 종속성 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52718-114">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="52718-115">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="52718-115">Invoke-AzResourceMoverBulkRemove</span></span>](Invoke-AzResourceMoverBulkRemove.md)
<span data-ttu-id="52718-116">이동 컬렉션에서 요청 본문에 포함된 이동 리소스 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="52718-116">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="52718-117">오케스트레이션은 서비스에 의해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="52718-117">The orchestration is done by service.</span></span>
<span data-ttu-id="52718-118">사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="52718-118">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="52718-119">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="52718-119">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="52718-120">요청 본문에 포함된 리소스 집합을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="52718-120">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="52718-121">커밋 작업은 moveState 'CommitPending' 또는 'CommitFailed'의 moveResources에서 트리거됩니다. 완료 시 moveResource moveState가 커밋으로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="52718-121">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="52718-122">사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="52718-122">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="52718-123">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="52718-123">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="52718-124">요청 본문에 포함된 리소스 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="52718-124">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="52718-125">삭제 작업은 moveState 'CommitPending' 또는 'DiscardFailed'의 moveResources에서 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 MovePending으로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="52718-125">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="52718-126">사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="52718-126">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="52718-127">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="52718-127">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="52718-128">요청 본문에 포함된 리소스 집합을 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="52718-128">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="52718-129">moveResources가 moveState 'MovePending' 또는 'MoveFailed'에 있는 후에 이동 작업이 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 커밋 보류로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="52718-129">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="52718-130">사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="52718-130">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="52718-131">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="52718-131">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="52718-132">시작은 요청 본문에 포함된 리소스 집합을 준비합니다.</span><span class="sxs-lookup"><span data-stu-id="52718-132">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="52718-133">준비 작업은 moveState 'PreparePending' 또는 'PrepareFailed'에 있는 moveResources에 있습니다. 성공적으로 완료 시 moveResource moveState에서 MovePending으로 전환을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="52718-133">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="52718-134">사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="52718-134">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="52718-135">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="52718-135">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="52718-136">이동 컬렉션을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="52718-136">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="52718-137">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="52718-137">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="52718-138">이동 컬렉션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="52718-138">Deletes a move collection.</span></span>

### [<span data-ttu-id="52718-139">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="52718-139">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="52718-140">이동 컬렉션에서 리소스 이동을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="52718-140">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="52718-141">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="52718-141">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="52718-142">이동 컬렉션에서 moveResources의 종속성 계산, 해결 및 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="52718-142">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

