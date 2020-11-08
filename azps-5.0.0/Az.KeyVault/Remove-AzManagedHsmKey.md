---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
ms.openlocfilehash: 15a9466dd0caac6ebe7497942de36e832b89ee55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215289"
---
# Remove-AzManagedHsmKey

## SYNOPSIS
관리 되는 HSM에서 키를 삭제 합니다.

## 구문과

### RemoveByKeyNameParameterSet (기본값)
```
Remove-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByInputObjectParameterSet
```
Remove-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
Remove-AzManagedHsmKey cmdlet은 관리 되는 HSM에서 키를 삭제 합니다.
키를 실수로 삭제 한 경우 특정 ' 복구 ' 권한이 있는 사용자가 Undo-AzManagedHsmKeyRemoval를 사용 하 여 키를 복구할 수 있습니다.
이 cmdlet의 값은 ' a/or **영향** ' 속성에 대해 high입니다.

## 예제의

### 예제 1: 관리 되는 HSM에서 키 제거
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -PassThru

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:35:06 AM
Scheduled Purge Date : 1/12/2021 9:35:06 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

이 명령은 testmhsm 이라는 관리 되는 HSM에서 testkey 라는 키를 제거 합니다.

### 예제 2: 사용자 확인 없이 키 제거
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -Force
```

이 명령은 testmhsm 이라는 관리 되는 HSM에서 testkey 라는 키를 제거 합니다.
명령에서 *Force* 매개 변수를 지정 하므로 cmdlet이 확인 메시지를 표시 하지 않습니다.

### 예제 3: 관리 되는 HSM에서 삭제 된 키 지우기 영구 제거
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState
```

이 명령은 testmhsm 이라는 관리 되는 HSM에서 testkey 라는 키를 영구적으로 제거 합니다.
이 cmdlet을 실행 하려면이 관리 되는 HSM에 대해 사용자에 게 명시적으로 부여 된 ' 제거 ' 권한이 필요 합니다.

### 예제 4: 파이프라인 연산자를 사용 하 여 키 제거
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzManagedHsmKey
```

이 명령은 관리 되는 HSM의 모든 키를 testmhsm 이라고 하 고 파이프라인 연산자를 사용 하 여 **Where-개체** cmdlet에 전달 합니다.
해당 cmdlet은 **Enabled** 특성에 대 한 $False 값을 갖는 키를 현재 cmdlet에 전달 합니다.
해당 cmdlet은 해당 키를 제거 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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
확인 메시지를 표시 하지 않습니다.

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

### -HsmName
HSM 이름. Cmdlet은 이름 및 현재 선택 된 환경에 따라 관리 되는 HSM의 FQDN을 생성 합니다.

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Key 개체

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
이전에 삭제 된 키를 영구적으로 제거 합니다.

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

### -이름
키 이름입니다.
Cmdlet은 관리 되는 HSM 이름, 현재 선택 된 환경 및 키 이름에서 키의 FQDN을 생성 합니다.

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Cmdlet은 기본적으로 개체를 반환 하지 않습니다.
이 스위치가 지정 된 경우 cmdlet은 삭제 된 키 개체를 반환 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### Microsoft. KeyVault. PSKeyVaultKeyIdentityItem

## 출력

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey

## 상속자

## 관련 링크

[추가-AzManagedHsmKey](./Add-AzManagedHsmKey.md)

[백업-AzManagedHsmKey](./Backup-AzManagedHsmKey.md)

[Get-AzManagedHsmKey](./Get-AzManagedHsmKey.md)

[실행 취소-AzManagedHsmKeyRemoval](./Undo-AzManagedHsmKeyRemoval.md)

[업데이트-AzManagedHsmKey](./Update-AzManagedHsmKey.md)

[Restore-AzManagedHsmKey](./Restore-AzManagedHsmKey.md)