---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 77f6ac36f756e89859d38a0c608139dfe28c9667
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954587"
---
# Set-AzKeyVaultAccessPolicy

## SYNOPSIS
키 자격 증명 모음을 사용하여 작업을 수행하도록 사용자, 애플리케이션 또는 보안 그룹에 대한 기존 사용 권한을 부여하거나 수정합니다.

## 구문

### ByUserPrincipalName(기본값)
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

## 설명
**Set-AzKeyVaultAccessPolicy** cmdlet은 키 자격 증명 모음을 사용하여 지정된 작업을 수행하기 위해 사용자, 애플리케이션 또는 보안 그룹에 대한 기존 권한을 부여하거나 수정합니다. 다른 사용자, 애플리케이션 또는 보안 그룹이 키 자격 증명 모음에 있는 권한을 수정하지 않습니다.
보안 그룹에 대한 사용 권한을 설정하는 경우 이 작업은 해당 보안 그룹의 사용자에만 영향을 미치게 됩니다.
다음 디렉터리는 모두 동일한 Azure 디렉터리가 되어야 합니다.
- 키 자격 증명 모음이 있는 Azure 구독의 기본 디렉터리입니다.
- 권한을 부여하는 사용자 또는 애플리케이션 그룹을 포함하는 Azure 디렉터리입니다.
이러한 조건을 충족하지 못하고 이 cmdlet이 작동하지 않는 시나리오의 예는 다음과 같습니다.
- 다른 조직의 사용자가 키 자격 증명 모음을 관리할 수 있도록 권한을 제공합니다.
각 조직에는 자체 디렉터리가 있습니다.
- Azure 계정에는 여러 개의 감독이 있습니다.
기본 디렉터리가 다른 디렉터리에 애플리케이션을 등록하는 경우 해당 애플리케이션이 키 자격 증명 모음을 사용할 수 있도록 권한을 승인할 수 없습니다.
애플리케이션은 기본 디렉터리에 있어야 합니다.
이 cmdlet에서는 리소스 그룹을 지정하는 것이 선택 사항이지만 성능을 향상하기 위해 이 작업을 해야 합니다.

> [!NOTE]
> 서비스 주체를 사용하여 액세스 정책 권한을 부여하는 경우 매개 변수를 사용해야 `-BypassObjectIdValidation` 합니다.

## 예제

### 예제 1: 키 자격 증명 모음에 대한 사용자에게 권한 부여 및 사용 권한 수정
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

첫 번째 명령은 Azure Active Directory의 사용자에게 Contoso03Vault라는 키 자격 증명 모음을 사용하여 키 및 비밀에 대한 작업을 수행할 수 있는 권한을 PattiFuller@contoso.com 부여합니다. *PassThru 매개* 변수는 cmdlet에서 업데이트된 개체를 반환합니다.
두 번째 명령은 첫 번째 명령에서 부여된 권한을 수정하여 이제 비밀을 설정하고 삭제하는 것 외에도 비밀을 지울 PattiFuller@contoso.com 수 있도록 합니다. 키 작업에 대한 사용 권한은 이 명령 이후에 변경되지 않습니다.
최종 명령은 키 작업에 대한 모든 권한을 제거하기 위한 기존 권한을 PattiFuller@contoso.com 추가로 수정합니다. 비밀 작업에 대한 사용 권한은 이 명령 후에 변경되지 않습니다.

### 예제 2: 애플리케이션 서비스 주체가 비밀을 읽고 쓸 수 있는 권한 부여
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

이 명령은 Contoso03Vault라는 키 자격 증명 모음에 대한 애플리케이션에 대한 권한을 부여합니다.
*ServicePrincipalName 매개 변수는* 애플리케이션을 지정합니다. 애플리케이션을 Azure Active Directory에 등록해야 합니다. *ServicePrincipalName* 매개 변수의 값은 애플리케이션의 서비스 주체 이름 또는 애플리케이션 ID GUID가 되어야 합니다.
이 예제에서는 서비스 주체 이름을 지정하며 명령은 비밀을 읽고 쓸 수 있는 애플리케이션 권한을 `http://payroll.contoso.com` 부여합니다.

### 예제 3: 개체 ID를 사용하여 애플리케이션에 대한 권한 부여
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

이 명령은 애플리케이션에게 비밀을 읽고 쓸 수 있는 권한을 부여합니다.
이 예제에서는 애플리케이션의 서비스 주체의 개체 ID를 사용하여 애플리케이션을 지정합니다.

### 예제 4: 사용자 주체 이름에 대한 권한 부여
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

이 명령은 비밀에 대한 액세스에 대해 지정된 사용자 주체 이름에 대한 권한을 얻게, 나열하고, 설정할 수 있습니다.

### 예제 5: Microsoft.Compute 리소스 공급자가 키 자격 증명 모음에서 비밀을 검색하도록 설정
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

이 명령은 Microsoft.Compute 리소스 공급자가 Contoso03Vault 키 자격 증명 모음에서 검색할 수 있는 권한을 부여합니다.

### 예제 6: 보안 그룹에 권한 부여
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

첫 번째 명령은 Get-AzADGroup cmdlet을 사용하여 모든 Active Directory 그룹을 얻습니다. 출력에서 **그룹1, group2** 및 **group3이라는** 3개 그룹이 **반환됩니다.** 여러 그룹에는 이름이 같지만 항상 고유한 ObjectId가 있을 수 있습니다. 이름이 같은 두 개 이상의 그룹이 반환되는 경우 출력의 ObjectId를 사용하여 사용할 그룹을 식별합니다.
그런 다음 이 명령의 출력을 Set-AzKeyVaultAccessPolicy **myownvault라는** 키 자격 증명 모음에 대한 group2에 대한 권한을 부여합니다. 이 예제에서는 동일한 명령줄에 'group2' 인라인이라는 그룹을 열소합니다.
반환된 목록에 'group2'라는 그룹이 여러 개 있을 수 있습니다.
이 예제에서는 반환된 목록에서 인덱스 0으로 표시된 첫 번째를 \[ \] 선택합니다.

### 예제 7: BYOK(고객 관리 테넌트 키에 대한 Azure Information Protection 액세스 권한 부여)
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

이 명령은 Azure Information Protection에서 고객 관리 키(사용자 키 가져오기 또는 "BYOK" 시나리오)를 Azure Information Protection 테넌트 키로 사용할 수 있도록 권한을 Azure Information Protection에 권한을 줍니다.
이 명령을 실행할 때 사용자 지정 키 자격 증명 모음 이름을 지정하지만 GUID **000000012-0000-c0000-000000000000000으로** *ServicePrincipalName* 매개 변수를 지정하고 예제에서 사용 권한을 지정해야 합니다.

## 매개 변수

### -ApplicationId
향후 사용할 수 있습니다.

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
Azure Active Directory에 개체가 존재하는지 확인하지 않고 개체 ID를 지정할 수 있습니다.
다른 Azure 테넌트에서 위임된 보안 그룹을 참조하는 개체 ID에 대한 키 자격 증명 모음에 대한 액세스 권한을 부여하려는 경우만 이 매개 변수를 사용합니다.

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
azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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
권한을 부여할 사용자의 사용자 전자 메일 주소를 지정합니다.
이 전자 메일 주소는 현재 구독과 연결된 디렉터리에 있어야 합니다.

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
가상 머신을 만들 때와 같은 리소스 만들기에서 이 키 자격 증명 모음을 참조할 때 Microsoft.Compute 리소스 공급자가 이 키 자격 증명 모음에서 비밀을 검색할 수 있습니다.

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
Azure 디스크 암호화 서비스를 사용하여 이 키 자격 증명 모음에서 비밀을 얻고 키를 래프 래프할 수 있습니다.

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
이 키 자격 증명 모음이 템플릿 배포에서 참조될 때 Azure Resource Manager가 이 키 자격 증명 모음에서 비밀을 얻을 수 있습니다.

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
Key Vault 개체

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
권한을 부여할 Azure Active Directory의 사용자 또는 서비스 주체의 개체 ID를 지정합니다.

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
작업하는 항목을 나타내는 개체를 반환합니다.
기본적으로 이 cmdlet은 출력을 생성하지 않습니다.

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
사용자 또는 서비스 주체에 부여할 인증서 사용 권한 배열을 지정합니다.
이 매개 변수에 대해 허용되는 값:
- 모두
- 가져오기
- 목록
- 삭제
- 만들기
- 가져오기
- 업데이트
- 관리contacts
- Getissuers
- Listissuers
- Setissuers
- Deleteissuers
- Manageissuers
- 복구
- 백업
- 복원
- 제거

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionsToKeys
사용자 또는 서비스 주체에 부여할 키 작업 권한의 배열을 지정합니다.
이 매개 변수에 대해 허용되는 값:
- 모두
- 암호 해독
- 암호화
- UnwrapKey
- WrapKey
- 확인
- 서명
- 가져오기
- 목록
- 업데이트
- 만들기
- 가져오기
- 삭제
- 백업
- 복원
- 복구
- 제거

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionsToSecrets
사용자 또는 서비스 주체에 부여할 비밀 작업 사용 권한 배열을 지정합니다.
이 매개 변수에 대해 허용되는 값:
- 모두
- 가져오기
- 목록
- 설정
- 삭제
- 백업
- 복원
- 복구
- 제거

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionsToStorage
사용자 또는 서비스 주체에 부여할 관리 저장소 계정 및 SaS-definition 작업 권한을 지정합니다.
이 매개 변수에 대해 허용되는 값:
- 모든
- 가져오기
- 목록
- delete
- 집합
- 업데이트
- regeneratekey
- getsas
- listsas
- deletesas
- setas
- 복구
- Backup
- 복원
- 제거

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름을 지정합니다.

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
Key Vault 리소스 ID

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
권한을 부여할 애플리케이션의 서비스 주체 이름을 지정합니다.
AzureActive Directory에서 애플리케이션에 등록된 클라이언트 ID라고도 하는 애플리케이션 ID를 지정합니다. 이 매개 변수가 지정하는 서비스 주체 이름이 있는 애플리케이션은 현재 구독을 포함하는 Azure 디렉터리에 등록해야 합니다.

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
권한을 부여할 사용자의 사용자 주체 이름을 지정합니다.
이 사용자 주체 이름은 현재 구독과 연결된 디렉터리에 있어야 합니다.

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
키 자격 증명 모음의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 키 자격 증명 모음에 대한 액세스 정책을 수정합니다.

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
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다. cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem

### System.String

## 출력

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

## 참고 사항

## 관련 링크

[Get-AzKeyVault](./Get-AzKeyVault.md)

[Remove-AzKeyVaultAccessPolicy](./Remove-AzKeyVaultAccessPolicy.md)

