---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377889"
---
# <span data-ttu-id="75e60-101">Az.ResourceMover 모듈</span><span class="sxs-lookup"><span data-stu-id="75e60-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="75e60-102">설명</span><span class="sxs-lookup"><span data-stu-id="75e60-102">Description</span></span>
<span data-ttu-id="75e60-103">Microsoft Azure PowerShell: ResourceMover cmdlet</span><span class="sxs-lookup"><span data-stu-id="75e60-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="75e60-104">Az.ResourceMover Cmdlet</span><span class="sxs-lookup"><span data-stu-id="75e60-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="75e60-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="75e60-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="75e60-106">이동 컬렉션에서 이동 리소스를 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="75e60-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="75e60-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="75e60-108">이동 컬렉션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-108">Gets the move collection.</span></span>

### [<span data-ttu-id="75e60-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="75e60-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="75e60-110">이동 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="75e60-111">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="75e60-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="75e60-112">해결되지 않은 종속성 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="75e60-113">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="75e60-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="75e60-114">요청 본문에 포함된 리소스 집합을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="75e60-115">moveResource moveState가 성공적으로 완료되면 moveState 'CommitPending' 또는 'CommitFailed'의 moveResources에서 커밋 작업이 트리거됩니다. moveResource moveState는 Committed로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="75e60-116">사용자가 작업을 전제로 하는 작업을 지원하기 위해 클라이언트는 validateOnly 속성이 true로 설정된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="75e60-117">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="75e60-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="75e60-118">요청 본문에 포함된 리소스 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="75e60-119">삭제 작업은 moveState 'CommitPending' 또는 'DiscardFailed'의 moveResources에서 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 MovePending으로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="75e60-120">사용자가 작업을 전제로 하는 작업을 지원하기 위해 클라이언트는 validateOnly 속성이 true로 설정된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="75e60-121">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="75e60-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="75e60-122">요청 본문에 포함된 리소스 집합을 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="75e60-123">moveResources가 moveState 'MovePending' 또는 'MoveFailed'에 있는 후 이동 작업이 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 커밋 보류로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="75e60-124">사용자가 작업을 전제로 하는 작업을 지원하기 위해 클라이언트는 validateOnly 속성이 true로 설정된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="75e60-125">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="75e60-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="75e60-126">요청 본문에 포함된 리소스 집합에 대한 준비를 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="75e60-127">prepare 작업은 moveState 'PreparePending' 또는 'PrepareFailed'에 있는 moveResources에 있습니다. 성공적으로 완료하면 moveResource moveState가 MovePending으로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="75e60-128">사용자가 작업을 전제로 하는 작업을 지원하기 위해 클라이언트는 validateOnly 속성이 true로 설정된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="75e60-129">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="75e60-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="75e60-130">이동 컬렉션을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="75e60-131">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="75e60-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="75e60-132">이동 컬렉션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="75e60-133">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="75e60-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="75e60-134">이동 컬렉션에서 리소스 이동을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="75e60-135">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="75e60-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="75e60-136">이동 컬렉션에서 moveResources의 종속성 계산, 확인 및 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="75e60-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

