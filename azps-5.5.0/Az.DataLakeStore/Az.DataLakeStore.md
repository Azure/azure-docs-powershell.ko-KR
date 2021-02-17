---
Module Name: Az.DataLakeStore
Module Guid: 90dfd814-abce-4e1f-99b6-fe16760c079a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Az.DataLakeStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Az.DataLakeStore.md
ms.openlocfilehash: 5796a3692274db9b49ed16c00935ed1cd2d4e8f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186172"
---
# Az.DataLakeStore 모듈
## 설명
이 섹션의 항목에서는 Azure Resource Manager(ARM) 프레임워크의 Azure Data Lake Store용 Azure PowerShell cmdlet을 설명합니다. cmdlet은 Microsoft.Azure.Commands.DataLakeStore 네임스페이스에 있습니다. 이러한 cmdlet은 Azure Data Lake Storage Gen1 계정에서만 작동됩니다.

## Az.DataLakeStore Cmdlet
### [Add-AzDataLakeStoreFirewallRule](Add-AzDataLakeStoreFirewallRule.md)
지정된 Data Lake Store 계정에 방화벽 규칙을 추가합니다.

### [Add-AzDataLakeStoreItemContent](Add-AzDataLakeStoreItemContent.md)
Data Lake Store의 항목에 콘텐츠를 추가합니다.

### [Add-AzDataLakeStoreTrustedIdProvider](Add-AzDataLakeStoreTrustedIdProvider.md)
지정된 Data Lake Store 계정에 신뢰할 수 있는 ID 공급자를 추가합니다.

### [Add-AzDataLakeStoreVirtualNetworkRule](Add-AzDataLakeStoreVirtualNetworkRule.md)
지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.

### [Enable-AzDataLakeStoreKeyVault](Enable-AzDataLakeStoreKeyVault.md)
지정된 Data Lake Store 계정의 암호화를 위해 사용자 관리 Key Vault를 사용하도록 설정하려고 시도합니다.

### [Export-AzDataLakeStoreChildItemProperty](Export-AzDataLakeStoreChildItemProperty.md)
지정된 경로에서 출력 경로로 전체 트리의 속성(디스크 사용량 및 Acl)을 내보낼 수 있습니다.

### [Export-AzDataLakeStoreItem](Export-AzDataLakeStoreItem.md)
Data Lake Store에서 파일을 다운로드합니다.

### [Get-AzDataLakeStoreAccount](Get-AzDataLakeStoreAccount.md)
Data Lake Store 계정의 세부 정보를 얻습니다.

### [Get-AzDataLakeStoreChildItem](Get-AzDataLakeStoreChildItem.md)
Data Lake Store의 폴더에 있는 항목 목록을 얻습니다.

### [Get-AzDataLakeStoreChildItemSummary](Get-AzDataLakeStoreChildItemSummary.md)
지정된 경로에 포함된 총 크기, 파일 및 원장의 요약을 얻습니다.

### [Get-AzDataLakeStoreFirewallRule](Get-AzDataLakeStoreFirewallRule.md)
지정된 Data Lake Store에서 지정된 방화벽 규칙을 얻습니다.
방화벽 규칙이 지정되지 않은 경우 계정에 대한 모든 방화벽 규칙을 나열합니다.

### [Get-AzDataLakeStoreItem](Get-AzDataLakeStoreItem.md)
Data Lake Store에서 파일 또는 폴더의 세부 정보를 얻습니다.

### [Get-AzDataLakeStoreItemAclEntry](Get-AzDataLakeStoreItemAclEntry.md)
Data Lake Store에서 파일 또는 폴더의 ACL에 있는 항목을 얻습니다.

### [Get-AzDataLakeStoreItemContent](Get-AzDataLakeStoreItemContent.md)
Data Lake Store에서 파일의 내용을 얻습니다.

### [Get-AzDataLakeStoreItemOwner](Get-AzDataLakeStoreItemOwner.md)
Data Lake Store에서 파일 또는 폴더의 소유자를 얻습니다.

### [Get-AzDataLakeStoreItemPermission](Get-AzDataLakeStoreItemPermission.md)
Data Lake Store에서 파일 또는 폴더의 사용 권한 8진수 권한을 얻습니다.

### [Get-AzDataLakeStoreTrustedIdProvider](Get-AzDataLakeStoreTrustedIdProvider.md)
지정된 Data Lake Store에서 지정된 신뢰할 수 있는 ID 공급자를 얻습니다.
공급자를 지정하지 않으면 계정에 대한 모든 공급자를 나열합니다.

### [Get-AzDataLakeStoreVirtualNetworkRule](Get-AzDataLakeStoreVirtualNetworkRule.md)
지정된 Data Lake Store에서 지정된 가상 네트워크 규칙을 얻습니다.
가상 네트워크 규칙을 지정하지 않으면 계정에 대한 모든 가상 네트워크 규칙을 나열합니다.

### [Import-AzDataLakeStoreItem](Import-AzDataLakeStoreItem.md)
Data Lake Store에 로컬 파일 또는 디렉터리를 업로드합니다.

### [Join-AzDataLakeStoreItem](Join-AzDataLakeStoreItem.md)
하나 이상의 파일을 조인하여 Data Lake Store에서 파일을 하나 만들 수 있습니다.

### [Move-AzDataLakeStoreItem](Move-AzDataLakeStoreItem.md)
Data Lake Store에서 파일 또는 폴더를 이동하거나 이름을 변경합니다.

### [New-AzDataLakeStoreAccount](New-AzDataLakeStoreAccount.md)
새 Data Lake Store 계정을 만듭니다.

### [New-AzDataLakeStoreItem](New-AzDataLakeStoreItem.md)
Data Lake Store에 새 파일 또는 폴더를 만듭니다.

### [Remove-AzDataLakeStoreAccount](Remove-AzDataLakeStoreAccount.md)
Data Lake Store 계정을 영구적으로 삭제합니다.

### [Remove-AzDataLakeStoreFirewallRule](Remove-AzDataLakeStoreFirewallRule.md)
지정된 Data Lake Store에서 지정된 방화벽 규칙을 제거합니다.

### [Remove-AzDataLakeStoreItem](Remove-AzDataLakeStoreItem.md)
Data Lake Store에서 파일 또는 폴더를 삭제합니다.

### [Remove-AzDataLakeStoreItemAcl](Remove-AzDataLakeStoreItemAcl.md)
Data Lake Store에서 파일 또는 폴더의 ACL을 지워야 합니다.

### [Remove-AzDataLakeStoreItemAclEntry](Remove-AzDataLakeStoreItemAclEntry.md)
Data Lake Store에서 파일 또는 폴더의 ACL에서 항목을 제거합니다.

### [Remove-AzDataLakeStoreTrustedIdProvider](Remove-AzDataLakeStoreTrustedIdProvider.md)
지정된 Data Lake Store에서 지정된 신뢰할 수 있는 ID 공급자를 제거합니다.

### [Remove-AzDataLakeStoreVirtualNetworkRule](Remove-AzDataLakeStoreVirtualNetworkRule.md)
지정된 Data Lake Store에서 지정된 가상 네트워크 규칙을 제거합니다.

### [Set-AzDataLakeStoreAccount](Set-AzDataLakeStoreAccount.md)
Data Lake Store 계정을 수정합니다.

### [Set-AzDataLakeStoreFirewallRule](Set-AzDataLakeStoreFirewallRule.md)
지정된 Data Lake Store에서 지정된 방화벽 규칙을 수정합니다.

### [Set-AzDataLakeStoreItemAcl](Set-AzDataLakeStoreItemAcl.md)
Data Lake Store에서 파일 또는 폴더의 ACL을 수정합니다.

### [Set-AzDataLakeStoreItemAclEntry](Set-AzDataLakeStoreItemAclEntry.md)
Data Lake Store에서 파일 또는 폴더의 ACL에 있는 항목을 수정합니다.

### [Set-AzDataLakeStoreItemExpiry](Set-AzDataLakeStoreItemExpiry.md)
Azure Data Lake Store 계정의 파일에 대한 만료 시간을 설정하거나 제거합니다.

### [Set-AzDataLakeStoreItemOwner](Set-AzDataLakeStoreItemOwner.md)
Data Lake Store에서 파일 또는 폴더의 소유자를 수정합니다.

### [Set-AzDataLakeStoreItemPermission](Set-AzDataLakeStoreItemPermission.md)
Data Lake Store에서 파일 또는 폴더의 사용 권한 8진수 권한을 수정합니다.

### [Set-AzDataLakeStoreTrustedIdProvider](Set-AzDataLakeStoreTrustedIdProvider.md)
지정된 Data Lake Store에서 지정된 신뢰할 수 있는 ID 공급자를 수정합니다.

### [Set-AzDataLakeStoreVirtualNetworkRule](Set-AzDataLakeStoreVirtualNetworkRule.md)
지정된 Data Lake Store에서 지정된 가상 네트워크 규칙을 수정합니다.

### [Test-AzDataLakeStoreAccount](Test-AzDataLakeStoreAccount.md)
Data Lake Store 계정의 존재를 테스트합니다.

### [Test-AzDataLakeStoreItem](Test-AzDataLakeStoreItem.md)
Data Lake Store에서 파일 또는 폴더의 존재를 테스트합니다.

