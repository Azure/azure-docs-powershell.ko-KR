---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491231"
---
# Az.StorageSync 모듈
## 설명
저장소 동기화 모듈의 cmdlet을 사용하면 PowerShell에서 Azure 파일 동기화와 같은 작업을 관리할 수 있습니다.

## Az.StorageSync Cmdlet
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
이 명령은 주어진 동기화 그룹 내의 모든 클라우드 엔드포인트를 나열합니다.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
이 명령은 주어진 저장소 동기화 서비스 내의 모든 동기화 그룹을 나열합니다.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
이 명령은 주어진 저장소 동기화 서비스에 등록된 모든 서버를 나열합니다.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
이 명령은 주어진 동기화 그룹 내의 모든 서버 엔드포인트를 나열합니다.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
이 명령은 구독/리소스 그룹의 주어진 범위 내에 있는 모든 저장소 동기화 서비스를 나열합니다.

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
이 명령을 사용하여 네임스페이스 변경 내용의 검색을 수동으로 시작할 수 있습니다. 전체 공유, 하위 폴더 또는 파일 집합을 대상으로 할 수 있습니다. 최대 10,000개 변경 내용을 검색할 수 있습니다. 변경 범위가 알려진 경우 이 명령의 실행을 네임스페이스의 일부로 제한하여 변경 검색을 10,000개 변경 제한 내에서 빠르게 완료할 수 있습니다.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
시스템과 Azure 파일 동기화 간의 잠재적인 호환성 문제를 확인합니다.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
이 명령은 모든 계층화 파일을 로컬 디스크로 회수합니다.

### [New-AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
이 명령은 동기화 그룹에 Azure 파일 동기화 클라우드 엔드포인트를 만듭니다.

### [New-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
이 명령은 지정된 저장소 동기화 서비스 내에 새 동기화 그룹을 만듭니다.

### [New-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
이 명령은 등록된 서버에 새 서버 엔드포인트를 만듭니다. 이렇게 하면 서버의 지정된 경로가 동기화 그룹의 다른 엔드포인트와 파일 동기화를 시작할 수 있습니다.

### [New-AzStorageSyncService](New-AzStorageSyncService.md)
이 명령은 리소스 그룹에 새 저장소 동기화 서비스를 만듭니다.

### [Set-AzStorageSyncService](New-AzStorageSyncService.md)
이 명령은 리소스 그룹에서 저장소 동기화 서비스를 설정합니다.

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
이 명령은 신뢰 관계를 만드는 저장소 동기화 서비스에 서버를 등록합니다. 그런 다음 PowerShell 또는 Azure Portal을 사용하여 이 서버에서 동기화를 구성할 수 있습니다.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
이 명령은 동기화 그룹에서 지정된 클라우드 엔드포인트를 삭제합니다. 하나 이상의 클라우드 엔드포인트가 없는 경우 이 동기화 그룹의 다른 서버 엔드포인트는 동기화할 수 없습니다.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
이 명령은 지정된 동기화 그룹을 삭제합니다.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
이 명령은 지정된 서버 엔드포인트를 삭제합니다. 이 위치에 동기화하면 즉시 중지됩니다.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
이 명령은 지정된 저장소 동기화 서비스를 삭제합니다.

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
문제 해결에만 사용 이 명령은 저장소 동기화 서비스에 서버 ID를 설명하는 데 사용되는 저장소 동기화 서버 인증서를 롤링합니다.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
이 명령을 사용하면 서버 엔드포인트의 조정 가능한 매개 변수를 변경할 수 있습니다.

### [Unregister-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
경고: 서버를 등록하지 않은 경우 이 서버의 모든 서버 엔드포인트가 모두 삭제됩니다. 이 명령은 저장소 동기화 서비스에서 서버를 등록을 등록하지 않습니다.

