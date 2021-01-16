---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358779"
---
# Az.ResourceMover 모듈
## 설명
Microsoft Azure PowerShell: ResourceMover cmdlet

## Az.ResourceMover Cmdlet
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
이동 컬렉션에서 이동 리소스를 생성하거나 업데이트합니다.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
이동 컬렉션을 얻습니다.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
이동 리소스를 얻습니다.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
해결되지 않은 종속성 목록을 얻습니다.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
요청 본문에 포함된 리소스 집합을 커밋합니다.
moveResource moveState가 성공적으로 완료되면 moveState 'CommitPending' 또는 'CommitFailed'의 moveResources에서 커밋 작업이 트리거됩니다. moveResource moveState는 Committed로 전환합니다.
사용자가 작업을 전제로 하는 작업을 지원하기 위해 클라이언트는 validateOnly 속성이 true로 설정된 작업을 호출할 수 있습니다.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
요청 본문에 포함된 리소스 집합을 삭제합니다.
삭제 작업은 moveState 'CommitPending' 또는 'DiscardFailed'의 moveResources에서 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 MovePending으로 전환합니다.
사용자가 작업을 전제로 하는 작업을 지원하기 위해 클라이언트는 validateOnly 속성이 true로 설정된 작업을 호출할 수 있습니다.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
요청 본문에 포함된 리소스 집합을 이동합니다.
moveResources가 moveState 'MovePending' 또는 'MoveFailed'에 있는 후 이동 작업이 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 커밋 보류로 전환합니다.
사용자가 작업을 전제로 하는 작업을 지원하기 위해 클라이언트는 validateOnly 속성이 true로 설정된 작업을 호출할 수 있습니다.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
요청 본문에 포함된 리소스 집합에 대한 준비를 초기화합니다.
prepare 작업은 moveState 'PreparePending' 또는 'PrepareFailed'에 있는 moveResources에 있습니다. 성공적으로 완료하면 moveResource moveState가 MovePending으로 전환합니다.
사용자가 작업을 전제로 하는 작업을 지원하기 위해 클라이언트는 validateOnly 속성이 true로 설정된 작업을 호출할 수 있습니다.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
이동 컬렉션을 생성하거나 업데이트합니다.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
이동 컬렉션을 삭제합니다.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
이동 컬렉션에서 리소스 이동을 삭제합니다.

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
이동 컬렉션에서 moveResources의 종속성 계산, 확인 및 유효성을 검사합니다.

