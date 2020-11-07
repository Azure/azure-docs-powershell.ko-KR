---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 3bfdc9c488f02794e82388741e7103417878c9f6
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/15/2019
ms.locfileid: "93689020"
---
# Az StorageSync 모듈
## 설명은
저장소 동기화 모듈의 cmdlet을 사용 하면 PowerShell의 Azure 파일 동기화와 관련 된 작업을 관리할 수 있습니다.

## Az StorageSync Cmdlet
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
이 명령은 지정 된 동기화 그룹 내의 모든 클라우드 끝점을 나열 합니다.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
이 명령은 지정 된 저장소 동기화 서비스 내의 모든 동기화 그룹을 나열 합니다.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
이 명령은 지정 된 저장소 동기화 서비스에 등록 된 모든 서버를 나열 합니다.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
이 명령은 지정 된 동기화 그룹 내의 모든 서버 끝점을 나열 합니다.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
이 명령은 구독/리소스 그룹의 지정 된 범위 내에 있는 모든 저장소 동기화 서비스를 나열 합니다.

### [AzStorageSyncChangeDetection-호출](Invoke-AzStorageSyncChangeDetection.md)
이 명령을 사용 하 여 네임 스페이스 변경 감지를 수동으로 시작할 수 있습니다. 전체 공유, 하위 폴더 또는 파일 집합을 대상으로 할 수 있습니다. 최대 1만 개의 변경 내용을 검색할 수 있습니다. 변경의 범위가 사용자에 게 알려진 경우이 명령의 실행을 네임 스페이스의 부분으로 제한 하 여 변경 내용이 1만 변경 제한 내에서 신속 하 게 완료 될 수 있도록 합니다.

### [AzStorageSyncCompatibilityCheck-호출](Invoke-AzStorageSyncCompatibilityCheck.md)
시스템 및 Azure 파일 동기화 간에 발생할 수 있는 호환성 문제가 있는지 확인 합니다.

### [AzStorageSyncFileRecall-호출](Invoke-AzStorageSyncFileRecall.md)
이 명령은 모든 계층화 파일을 다시 로컬 디스크로 회수 합니다.

### [새로운 AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
이 명령은 동기화 그룹에 Azure 파일 동기화 클라우드 끝점을 만듭니다.

### [새로운 AzStorageSyncGroup](New-AzStorageSyncGroup.md)
이 명령은 지정 된 저장소 동기화 서비스 내에 새 동기화 그룹을 만듭니다.

### [새로운 AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
이 명령은 등록 된 서버에서 새 서버 끝점을 만듭니다. 이렇게 하면 서버의 지정 된 경로가 동기화 그룹의 다른 끝점과 파일 동기화를 시작할 수 있습니다.

### [새로운 AzStorageSyncService](New-AzStorageSyncService.md)
이 명령은 리소스 그룹에 새 저장소 동기화 서비스를 만듭니다.

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
이 명령은 신뢰 관계를 만드는 저장소 동기화 서비스에 서버를 등록 합니다. 그러면 PowerShell 또는 Azure 포털을 사용 하 여이 서버에서 동기화를 구성할 수 있습니다.

### [제거-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
이 명령은 동기화 그룹에서 지정 된 클라우드 끝점을 삭제 합니다. 하나 이상의 클라우드 끝점이 없으면이 동기화 그룹의 다른 서버 끝점을 동기화 할 수 없습니다.

### [제거-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
이 명령은 지정 된 동기화 그룹을 삭제 합니다.

### [제거-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
이 명령은 지정 된 서버 종점을 삭제 합니다. 이 위치와 동기화가 즉시 중지 됩니다.

### [제거-AzStorageSyncService](Remove-AzStorageSyncService.md)
이 명령은 지정 된 저장소 동기화 서비스를 삭제 합니다.

### [다시 설정-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
문제 해결에만 사용 합니다. 이 명령은 저장소 동기화 서비스에 대 한 서버 id를 설명 하는 데 사용 되는 저장소 동기화 서버 인증서를 롤백합니다.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
이 명령을 사용 하 여 서버 끝점의 조정 가능한 매개 변수를 변경할 수 있습니다.

### [등록 취소-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
경고: 서버의 등록을 취소 하면이 서버의 모든 서버 끝점에 대 한 연계 삭제가 생성 됩니다. 이 명령은 저장소 동기화 서비스에서 서버의 등록을 취소 합니다.

