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
# Az.ResourceMover 모듈
## 설명
Microsoft Azure PowerShell: ResourceMover cmdlet

## Az.ResourceMover Cmdlet
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
이동 컬렉션에서 리소스 이동을 생성하거나 업데이트합니다.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
이동 컬렉션을 얻습니다.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
리소스 이동을 얻습니다.

### [Get-AzResourceMoverRequiredForResources](Get-AzResourceMoverRequiredForResources.md)
팔 리소스가 필요한 이동 리소스 목록입니다.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
해결되지 않은 종속성 목록을 얻습니다.

### [Invoke-AzResourceMoverBulkRemove](Invoke-AzResourceMoverBulkRemove.md)
이동 컬렉션에서 요청 본문에 포함된 이동 리소스 집합을 제거합니다.
오케스트레이션은 서비스에 의해 수행됩니다.
사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
요청 본문에 포함된 리소스 집합을 커밋합니다.
커밋 작업은 moveState 'CommitPending' 또는 'CommitFailed'의 moveResources에서 트리거됩니다. 완료 시 moveResource moveState가 커밋으로 전환합니다.
사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
요청 본문에 포함된 리소스 집합을 삭제합니다.
삭제 작업은 moveState 'CommitPending' 또는 'DiscardFailed'의 moveResources에서 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 MovePending으로 전환합니다.
사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
요청 본문에 포함된 리소스 집합을 이동합니다.
moveResources가 moveState 'MovePending' 또는 'MoveFailed'에 있는 후에 이동 작업이 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 커밋 보류로 전환합니다.
사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
시작은 요청 본문에 포함된 리소스 집합을 준비합니다.
준비 작업은 moveState 'PreparePending' 또는 'PrepareFailed'에 있는 moveResources에 있습니다. 성공적으로 완료 시 moveResource moveState에서 MovePending으로 전환을 수행합니다.
사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
이동 컬렉션을 생성하거나 업데이트합니다.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
이동 컬렉션을 삭제합니다.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
이동 컬렉션에서 리소스 이동을 삭제합니다.

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
이동 컬렉션에서 moveResources의 종속성 계산, 해결 및 유효성을 검사합니다.

