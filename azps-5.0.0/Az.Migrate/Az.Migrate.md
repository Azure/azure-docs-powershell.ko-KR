---
Module Name: Az.Migrate
Module Guid: c638312b-9fd1-4611-a5cc-11a8caa5b698
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.migrate
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Az.Migrate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Az.Migrate.md
ms.openlocfilehash: a98b0f52edec1ef4e26a359ffa5d16942dc52528
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218879"
---
# Az 마이그레이션 모듈
## 설명은
Microsoft Azure PowerShell: cmdlet 마이그레이션

## Az 마이그레이션 Cmdlet
### [Get-AzMigrateDiscoveredServer](Get-AzMigrateDiscoveredServer.md)
Azure 마이그레이션 서버 서비스 가져오기 프로젝트 마이그레이션에 있는 모든 서버를 페치합니다.

### [Get-AzMigrateJob](Get-AzMigrateJob.md)
Get-AzMigrateJob cmdlet retrives Azure 마이그레이션 작업의 상태를 보고 합니다.

### [Get-AzMigrateProject](Get-AzMigrateProject.md)
마이그레이션 프로젝트를 가져오는 메서드입니다.

### [Get-AzMigrateReplicationFabric](Get-AzMigrateReplicationFabric.md)
Azure Site Recovery 패브릭의 세부 정보를 가져옵니다.

### [Get-AzMigrateReplicationPolicy](Get-AzMigrateReplicationPolicy.md)
복제 정책의 세부 정보를 가져옵니다.

### [Get-AzMigrateReplicationProtectionContainer](Get-AzMigrateReplicationProtectionContainer.md)
보호 컨테이너의 세부 정보를 가져옵니다.

### [Get-AzMigrateReplicationProtectionContainerMapping](Get-AzMigrateReplicationProtectionContainerMapping.md)
보호 컨테이너 매핑의 세부 정보를 가져옵니다.

### [Get-AzMigrateReplicationRecoveryServicesProvider](Get-AzMigrateReplicationRecoveryServicesProvider.md)
등록 된 복구 서비스 공급자의 세부 정보를 가져옵니다.

### [Get-AzMigrateRunAsAccount](Get-AzMigrateRunAsAccount.md)
실행 계정을 가져오는 메서드입니다.

### [Get-AzMigrateServerReplication](Get-AzMigrateServerReplication.md)
Get-AzMigrateServerReplication cmdlet은 복제 서버의 개체를 검색 합니다.

### [Get-AzMigrateSite](Get-AzMigrateSite.md)
사이트를 가져오는 방법입니다.

### [Get-AzMigrateSolution](Get-AzMigrateSolution.md)
마이그레이션 프로젝트의 솔루션을 가져옵니다.

### [새로운 AzMigrateDiskMapping](New-AzMigrateDiskMapping.md)
New-AzMigrateDiskMapping cmdlet은 마이그레이션할 서버에 연결 된 원본 디스크의 매핑을 만듭니다.

### [새로운 AzMigrateNicMapping](New-AzMigrateNicMapping.md)
New-AzMigrateNicMapping cmdlet은 마이그레이션할 서버에 연결 된 원본 NIC의 매핑을 만듭니다.
이 개체는 복제 서버의 NIC 및 해당 속성을 업데이트 하는 Set-AzMigrateServerReplication cmdlet에 대 한 입력으로 제공 됩니다.

### [새로운 AzMigrateProject](New-AzMigrateProject.md)
새 마이그레이션 프로젝트를 만듭니다.

### [새로운 AzMigrateReplicationPolicy](New-AzMigrateReplicationPolicy.md)
복제 정책 만들기 작업

### [새로운 AzMigrateReplicationProtectionContainerMapping](New-AzMigrateReplicationProtectionContainerMapping.md)
보호 컨테이너 매핑을 만드는 작업입니다.

### [새로운 AzMigrateServerReplication](New-AzMigrateServerReplication.md)
New-AzMigrateServerReplication cmdlet은 Azure 마이그레이션 프로젝트에서 검색 된 특정 서버에 대 한 복제를 시작 합니다.

### [Register-AzMigrateProjectTool](Register-AzMigrateProjectTool.md)
마이그레이션 프로젝트에 도구를 등록 합니다.

### [제거-AzMigrateProject](Remove-AzMigrateProject.md)
마이그레이션 프로젝트를 삭제 합니다.
존재 하지 않는 프로젝트를 삭제 하는 것은 작업 없음입니다.

### [제거-AzMigrateServerReplication](Remove-AzMigrateServerReplication.md)
Remove-AzMigrateServerReplication cmdlet은 마이그레이션된 서버에 대 한 복제를 중지 합니다.

### [다시 시작-AzMigrateServerReplication](Restart-AzMigrateServerReplication.md)
Restart-AzMigrateServerReplication cmdlet은 지정 된 서버의 복제를 복구 합니다.

### [Set-AzMigrateServerReplication](Set-AzMigrateServerReplication.md)
Set-AzMigrateServerReplication cmdlet은 복제 서버의 대상 속성을 업데이트 합니다.

### [시작-AzMigrateServerMigration](Start-AzMigrateServerMigration.md)
복제 서버에 대 한 마이그레이션을 시작 합니다.

### [시작-AzMigrateTestMigration](Start-AzMigrateTestMigration.md)
Start-AzMigrateTestMigration cmdlet은 복제 서버에 대 한 테스트 마이그레이션을 시작 합니다.

### [시작-AzMigrateTestMigrationCleanup](Start-AzMigrateTestMigrationCleanup.md)
Start-AzMigrateTestMigrationCleanup cmdlet은 복제 서버에 대 한 테스트 마이그레이션 정리를 시작 합니다.

