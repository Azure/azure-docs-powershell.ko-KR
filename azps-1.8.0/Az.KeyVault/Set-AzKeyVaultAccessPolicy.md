---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 55cdc385c5cdf291db15399f4fd587b9b10ce308
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93883262"
---
# Set-AzKeyVaultAccessPolicy

## SYNOPSIS
키 자격 증명 모음을 사용 하 여 작업을 수행 하기 위해 사용자, 응용 프로그램 또는 보안 그룹에 대 한 기존 사용 권한을 부여 하거나 수정 합니다.

## 구문과

### ByUserPrincipalName (기본값)
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByObjectId
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServicePrincipalName
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByEmailAddress
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ForVault
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectByObjectId
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectByServicePrincipalName
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectByUserPrincipalName
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectByEmailAddress
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectForVault
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdByObjectId
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdByServicePrincipalName
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ResourceIdByUserPrincipalName
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdByEmailAddress
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdForVault
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzKeyVaultAccessPolicy** cmdlet은 사용자, 응용 프로그램 또는 보안 그룹의 기존 사용 권한을 부여 하거나 수정 하 여 키 자격 증명 모음으로 지정 된 작업을 수행 합니다. 다른 사용자, 앱 또는 보안 그룹의 키 자격 증명에 대 한 사용 권한은 수정 되지 않습니다.
보안 그룹에 대 한 사용 권한을 설정 하는 경우이 작업은 해당 보안 그룹의 사용자 에게만 적용 됩니다.
다음 디렉터리는 모두 동일한 Azure 디렉터리 여야 합니다.
- 키 보관소가 있는 Azure 구독의 기본 디렉터리입니다.
- 권한을 부여 하는 사용자 또는 응용 프로그램 그룹이 포함 된 Azure 디렉터리입니다.
이러한 조건이 충족 되지 않고이 cmdlet이 작동 하지 않을 경우 시나리오의 예:
- 다른 조직에서 사용자의 키 자격 증명을 관리 하도록 권한을 부여 합니다.
각 조직에는 고유한 디렉터리가 있습니다.
- Azure 계정에 디렉터리가 여러 개 있습니다.
기본 디렉터리가 아닌 디렉터리에 응용 프로그램을 등록 하는 경우 해당 응용 프로그램에 키 자격 증명 모음을 사용 하도록 허가할 수 없습니다.
응용 프로그램이 기본 디렉터리에 있어야 합니다.
이 cmdlet에 대해 리소스 그룹을 지정 하는 것은 선택 사항 이지만 성능 향상을 위해 이러한 작업을 수행 해야 한다는 점에 유의 하세요.

## 예제의

### 예제 1: 키 자격 증명 모음에 대 한 사용 권한을 사용자에 게 부여 하 고 사용 권한을 수정 합니다.
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :
```

첫 번째 명령은 Azure Active Directory의 사용자에 대 한 사용 권한을 부여 PattiFuller@contoso.com 하 고, Contoso03Vault 이라는 키 보관소를 사용 하 여 키 및 비밀에 대 한 작업을 수행 합니다. *PassThru* 매개 변수는 cmdlet에서 반환 되는 업데이트 된 개체를 생성 합니다.
두 번째 명령은 첫 번째 명령에 부여 된 사용 권한을 수정 하 여 PattiFuller@contoso.com , 이제 암호를 설정 하 고 삭제 하는 것 외에도 비밀을 받을 수 있도록 합니다. 이 명령 후에는 키 작업에 대 한 사용 권한이 변경 되지 않고 그대로 유지 됩니다.
마지막 명령은 PattiFuller@contoso.com 키 작업에 대 한 모든 사용 권한을 제거 하는 기존 권한을 추가로 수정 합니다. 이 명령 후에는 비밀 작업에 대 한 사용 권한이 변경 되지 않고 그대로 유지 됩니다.

### 예제 2: 비밀 정보를 읽고 쓸 수 있도록 응용 프로그램 서비스 사용자에 게 권한 부여
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

이 명령은 Contoso03Vault 이라는 키 보관소에 대 한 응용 프로그램에 대 한 사용 권한을 부여 합니다.
*ServicePrincipalName* 매개 변수는 응용 프로그램을 지정 합니다. Azure Active Directory에 응용 프로그램을 등록 해야 합니다. *ServicePrincipalName* 매개 변수 값은 응용 프로그램의 서비스 사용자 이름 또는 응용 프로그램 ID GUID 여야 합니다.
이 예제에서는 서비스 사용자 이름을 지정 하 `http://payroll.contoso.com` 고, 명령은 비밀 정보를 읽고 쓸 수 있도록 응용 프로그램 사용 권한을 부여 합니다.

### 예제 3: 해당 개체 ID를 사용 하 여 응용 프로그램에 대 한 사용 권한 부여
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

이 명령은 비밀 정보를 읽고 쓸 수 있도록 응용 프로그램 사용 권한을 부여 합니다.
이 예제에서는 응용 프로그램의 서비스 사용자에 대 한 개체 ID를 사용 하 여 응용 프로그램을 지정 합니다.

### 예제 4: 사용자 계정 이름에 대 한 사용 권한 부여
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

이 명령은 비밀에 대 한 액세스에 대 한 지정 된 upn (사용자 이름)의 get, list, set 권한을 부여 합니다.

### 예제 5: Microsoft에서 키 자격 증명 모음 으로부터 비밀을 검색 하도록 설정 합니다. 계산 리소스 공급자
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

이 명령은 Contoso03Vault 키 자격 증명 모음에서 Microsoft. a 리소스 공급자가 검색할 수 있는 비밀 정보에 대 한 사용 권한을 부여 합니다.

### 예제 6: 보안 그룹에 대 한 사용 권한 부여
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

첫 번째 명령은 Get-AzADGroup cmdlet을 사용 하 여 모든 Active Directory 그룹을 가져옵니다. 출력에서 이름이 **group1** , **group2** 및 **group3** 인 3 개의 그룹이 반환 됨을 볼 수 있습니다. 여러 그룹의 이름은 동일 하지만 항상 고유한 ObjectId를 가질 수 있습니다. 동일한 이름을 가진 그룹이 두 개 이상 반환 되는 경우 출력에 ObjectId를 사용 하 여 사용할 항목을 식별 합니다.
그런 다음이 명령의 출력을 Set-AzKeyVaultAccessPolicy와 함께 사용 하 여 **myownvault** 이라는 키 보관소의 group2에 대 한 사용 권한을 부여할 수 있습니다. 이 예제에서는 동일한 명령줄에서 ' group2 ' 이라는 그룹을 열거 합니다.
반환 된 목록에 이름이 ' group2 ' 인 여러 그룹이 있을 수 있습니다.
이 예제에서는 반환 된 목록의 인덱스 0으로 표시 되는 첫 번째 항목을 선택 \[ \] 합니다.

### 예제 7: 고객 관리 테 넌 트 키 (BYOK)에 대 한 Azure Information Protection 액세스 권한 부여
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

이 명령은 사용자가 관리 하는 키 (자체 키 가져오기 또는 "BYOK" 시나리오)를 Azure Information Protection 테 넌 트 키로 사용 하도록 Azure Information Protection에 권한을 부여 합니다.
이 명령을 실행할 때 고유한 키 보관소 이름을 지정 하면 *ServicePrincipalName* 매개 변수를 GUID **00000012-0000-0000-c 000-000000000000** 에 지정 하 고 예제에서 사용 권한을 지정 해야 합니다.

## 변수

### -ApplicationId
나중에 사용 합니다.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BypassObjectIdValidation
Azure Active Directory에 개체가 있는지 확인 하지 않고 개체 ID를 지정할 수 있도록 합니다.
다른 Azure 테 넌 트에서 위임 된 보안 그룹을 참조 하는 개체 ID에 키 자격 증명 모음에 대 한 액세스 권한을 부여 하려는 경우에만이 매개 변수를 사용 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EmailAddress
권한을 부여할 사용자의 사용자 전자 메일 주소를 지정 합니다.
이 전자 메일 주소는 현재 구독과 연결 된 디렉터리에 있어야 하 고 고유 해야 합니다.

```yaml
Type: System.String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress, ResourceIdByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForDeployment
이 키 자격 증명 모음이 리소스 만들기에서 참조 되는 경우 (예: 가상 컴퓨터를 만들 때)이 키 보관소에서 비밀을 검색 하도록 Microsoft. a 리소스 공급자를 설정 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForDiskEncryption
Azure 디스크 암호화 서비스에서이 키 자격 증명 모음의 비밀 및 래핑 키를 가져올 수 있도록 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForTemplateDeployment
이 키 자격 증명 모음이 서식 파일 배포에서 참조 되는 경우 Azure 리소스 관리자가이 키 보관소에서 비밀을 가져올 수 있도록 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
키 자격 증명 모음 개체

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
사용 권한을 부여할 Azure Active Directory의 사용자 또는 서비스 사용자의 개체 ID를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
작업 중인 항목을 나타내는 개체를 반환 합니다.
기본적으로이 cmdlet은 출력을 생성 하지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionsToCertificates
사용자 또는 서비스 사용자에 게 부여할 인증서 권한 배열을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 가져오기
- 목록
- 삭제
- 만드는
- Import
- Update
- Managecontacts
- Getissuers
- Listissuers
- Setissuers
- Deleteissuers
- Manageissuers
- 절약할
- 백업할
- 복원한
- 지우시겠습니까

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -기능 하는 Sto키
사용자 또는 서비스 사용자에 게 부여할 키 작업 사용 권한의 배열을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 해독은
- 해독할
- UnwrapKey
- WrapKey
- 나타나는지
- 등록할
- 가져오기
- 목록
- Update
- 만드는
- Import
- 삭제
- 백업할
- 복원한
- 절약할
- 지우시겠습니까

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -기능 방법 비밀
사용자 또는 서비스 사용자에 게 부여할 비밀 작업 권한 배열을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 가져오기
- 목록
- 설치할
- 삭제
- 백업할
- 복원한
- 절약할
- 지우시겠습니까

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -기능 저장 저장소
사용자 또는 서비스 사용자에 게 부여할 관리 되는 저장소 계정 및 SaS 정의 작업 사용 권한을 지정 합니다.

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
키 자격 증명 모음 리소스 Id

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
권한을 부여할 응용 프로그램의 서비스 사용자 이름을 지정 합니다.
클라이언트 ID 라고도 하는 응용 프로그램 ID를 AzureActive Directory의 응용 프로그램에 등록 하 여 지정 합니다. 이 매개 변수에서 지정 하는 서비스 사용자 이름을 사용 하는 응용 프로그램은 현재 구독을 포함 하는 Azure 디렉터리에 등록 되어 있어야 합니다.

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName, ResourceIdByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserPrincipalName
권한을 부여할 사용자의 upn (사용자 이름)을 지정 합니다.
이 사용자 사용자 이름은 현재 구독과 연결 된 디렉터리에 있어야 합니다.

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName, ResourceIdByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
키 보관소의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 키 보관소에 대 한 액세스 정책을 수정 합니다.

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft. KeyVault. PSKeyVaultIdentityItem

### System. 문자열

## 출력

### Microsoft. KeyVault. 모델. PSKeyVault

## 상속자

## 관련 링크

[Get-AzKeyVault](./Get-AzKeyVault.md)

[제거-AzKeyVaultAccessPolicy](./Remove-AzKeyVaultAccessPolicy.md)

