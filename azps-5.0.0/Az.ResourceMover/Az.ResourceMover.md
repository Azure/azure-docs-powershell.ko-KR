---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217548"
---
# 모듈 위의 Az
## 설명은
Microsoft Azure PowerShell: ResourceMover cmdlet

## A. a i a. ResourceMover
### [추가-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
이동 모음에서 이동 리소스를 만들거나 업데이트 합니다.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
이동 컬렉션을 가져옵니다.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
이동 리소스를 가져옵니다.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
해결 되지 않은 종속성의 목록을 가져옵니다.

### [AzResourceMoverCommit-호출](Invoke-AzResourceMoverCommit.md)
요청 본문에 포함 된 리소스 집합을 커밋합니다.
커밋 작업은 moveState ' CommitPending ' 또는 ' Commitpending '의 moveResources에 대해 트리거 되며 성공적으로 완료 되 면 moveResource moveState가 커밋으로 전환 됩니다.
사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.

### [AzResourceMoverDiscard-호출](Invoke-AzResourceMoverDiscard.md)
요청 본문에 포함 된 리소스 집합을 삭제 합니다.
취소 작업은 moveState ' CommitPending ' 또는 ' DiscardFailed '의 moveResources에 대해 트리거 되며 성공적으로 완료 되 면 moveResource moveState는 MovePending으로 전환 됩니다.
사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.

### [AzResourceMoverInitiateMove-호출](Invoke-AzResourceMoverInitiateMove.md)
요청 본문에 포함 된 리소스 집합을 이동 합니다.
이동 작업은 moveResources이 moveState ' MovePending ' 또는 ' MoveFailed '에 있는 후에 트리거 되며 성공적으로 완료 되 면 moveResource moveState가 CommitPending으로 전환 됩니다.
사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.

### [AzResourceMoverPrepare-호출](Invoke-AzResourceMoverPrepare.md)
요청 본문에 포함 된 리소스 집합에 대 한 준비를 시작 합니다.
준비 작업은 moveState ' PreparePending ' 또는 ' PrepareFailed ' 인 moveResources에 있으며 성공적으로 완료 되 면 moveResource moveState는 MovePending으로 전환 됩니다.
사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.

### [새로운 AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
이동 모음을 만들거나 업데이트 합니다.

### [제거-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
이동 모음을 삭제 합니다.

### [제거-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
이동 컬렉션에서 이동 리소스를 삭제 합니다.

### [해결-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
이동 컬렉션의 moveResources 종속성을 계산 하 고, 해결 하 고, 유효성을 검사 합니다.

