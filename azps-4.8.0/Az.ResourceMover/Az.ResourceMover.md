---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211948"
---
# <span data-ttu-id="9b41d-101">모듈 위의 Az</span><span class="sxs-lookup"><span data-stu-id="9b41d-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="9b41d-102">설명은</span><span class="sxs-lookup"><span data-stu-id="9b41d-102">Description</span></span>
<span data-ttu-id="9b41d-103">Microsoft Azure PowerShell: ResourceMover cmdlet</span><span class="sxs-lookup"><span data-stu-id="9b41d-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="9b41d-104">A. a i a. ResourceMover</span><span class="sxs-lookup"><span data-stu-id="9b41d-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="9b41d-105">추가-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="9b41d-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="9b41d-106">이동 모음에서 이동 리소스를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="9b41d-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="9b41d-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="9b41d-108">이동 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-108">Gets the move collection.</span></span>

### [<span data-ttu-id="9b41d-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="9b41d-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="9b41d-110">이동 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="9b41d-111">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="9b41d-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="9b41d-112">해결 되지 않은 종속성의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="9b41d-113">AzResourceMoverCommit-호출</span><span class="sxs-lookup"><span data-stu-id="9b41d-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="9b41d-114">요청 본문에 포함 된 리소스 집합을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="9b41d-115">커밋 작업은 moveState ' CommitPending ' 또는 ' Commitpending '의 moveResources에 대해 트리거 되며 성공적으로 완료 되 면 moveResource moveState가 커밋으로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="9b41d-116">사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="9b41d-117">AzResourceMoverDiscard-호출</span><span class="sxs-lookup"><span data-stu-id="9b41d-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="9b41d-118">요청 본문에 포함 된 리소스 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="9b41d-119">취소 작업은 moveState ' CommitPending ' 또는 ' DiscardFailed '의 moveResources에 대해 트리거 되며 성공적으로 완료 되 면 moveResource moveState는 MovePending으로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="9b41d-120">사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="9b41d-121">AzResourceMoverInitiateMove-호출</span><span class="sxs-lookup"><span data-stu-id="9b41d-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="9b41d-122">요청 본문에 포함 된 리소스 집합을 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="9b41d-123">이동 작업은 moveResources이 moveState ' MovePending ' 또는 ' MoveFailed '에 있는 후에 트리거 되며 성공적으로 완료 되 면 moveResource moveState가 CommitPending으로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="9b41d-124">사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="9b41d-125">AzResourceMoverPrepare-호출</span><span class="sxs-lookup"><span data-stu-id="9b41d-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="9b41d-126">요청 본문에 포함 된 리소스 집합에 대 한 준비를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="9b41d-127">준비 작업은 moveState ' PreparePending ' 또는 ' PrepareFailed ' 인 moveResources에 있으며 성공적으로 완료 되 면 moveResource moveState는 MovePending으로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="9b41d-128">사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="9b41d-129">새로운 AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="9b41d-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="9b41d-130">이동 모음을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="9b41d-131">제거-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="9b41d-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="9b41d-132">이동 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="9b41d-133">제거-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="9b41d-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="9b41d-134">이동 컬렉션에서 이동 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="9b41d-135">해결-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="9b41d-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="9b41d-136">이동 컬렉션의 moveResources 종속성을 계산 하 고, 해결 하 고, 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b41d-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

