---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: ab126ee6bfc6a19f4a3a9997a75a01277437e42d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952512"
---
# Remove-AzKeyVaultManagedStorageAccount

## SYNOPSIS
Key Vault 관리 Azure Storage 계정 및 연결된 모든 SAS 정의를 제거합니다.

## 구문

### ByDefinitionName(기본값)
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
Key Vault에서 Azure Storage 계정을 분해합니다. 이렇게 해서 Azure Storage 계정을 제거하지는 않지만 Azure Key Vault에서 계정 키를 관리하지 않습니다. 연결된 모든 Key Vault 관리 저장소 SAS 정의도 제거됩니다.

## 예제

### 예제 1: Key Vault 관리 Azure Storage 계정 및 연결된 모든 SAS 정의를 제거합니다.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

Key Vault 'myvault'에서 Azure Storage 계정 'mystorageaccount'를 분해하고 Key Vault가 해당 키를 관리하지 못하게 합니다. 'mystorageaccount' 계정은 제거되지 않습니다. 이 계정과 연결된 모든 Key Vault 관리 저장소 SAS 정의가 제거됩니다.

### 예제 2: 사용자 확인 없이 Key Vault 관리 Azure Storage 계정 및 연결된 모든 SAS 정의를 제거합니다.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

Key Vault 'myvault'에서 Azure Storage 계정 'mystorageaccount'를 분해하고 Key Vault가 해당 키를 관리하지 못하게 합니다. 'mystorageaccount' 계정은 제거되지 않습니다. 이 계정과 연결된 모든 Key Vault 관리 저장소 SAS 정의가 제거됩니다.

### 예제 3: Key Vault 관리 Azure Storage 계정 및 모든 연결된 SAS 정의를 영구적으로 삭제(제거)합니다.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

이 예제에서는 이 자격 증명 모음에 대해 소프트 삭제가 사용하도록 설정되어 있는 것으로 가정합니다. 자격 증명 모음 속성 또는 자격 증명 모음의 엔터티의 RecoveryLevel 특성을 검사하여 이러한 경우인지를 확인합니다.
첫 번째 cmdlet은 Key Vault 'myvault'에서 Azure Storage 계정 'mystorageaccount'를 분해하고 Key Vault에서 키를 관리하지 못하게 합니다. 'mystorageaccount' 계정은 제거되지 않습니다. 이 계정과 연결된 모든 Key Vault 관리 저장소 SAS 정의가 제거됩니다.
두 번째 cmdlet은 저장소 계정이 삭제되지만 복구 가능한 상태인지 확인합니다. 이 상태로 도달하는 데 다소 시간이 필요할 수 있습니다. 시도하기 전에 ~30초를 허용합니다.
세 번째 cmdlet은 저장소 계정을 영구적으로 제거합니다. 복구는 더 이상 불가능합니다.

## 매개 변수

### -AccountName
Key Vault 관리 저장소 계정 이름입니다. Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 맹그 저장소 계정 이름에서 관리되는 저장소 계정 이름의 FQDN을 생성합니다.

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
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

### -Force
확인을 요청하지 않습니다.

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

### -InputObject
ManagedStorageAccount 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
이전에 삭제된 관리되는 저장소 계정을 영구적으로 제거합니다.

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

### -PassThru
Cmdlet은 기본적으로 개체를 반환하지 않습니다.
이 스위치가 지정된 경우 cmdlet은 삭제된 관리되는 저장소 계정을 반환합니다.

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

### -VaultName
자격 증명 모음 이름입니다.
Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 생성합니다.

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다.

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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem

## 출력

### Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultManagedStorageAccount

## 참고 사항

## 관련 링크

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

