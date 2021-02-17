---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 3c5435d1a472341d0447ead2f384fa892d6e1202
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404482"
---
# Remove-AzKeyVaultKey

## SYNOPSIS
키 자격 증명 모음에서 키를 삭제합니다.

## 구문

### ByVaultName(기본값)
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmByVaultName
```
Remove-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
Remove-AzKeyVaultKey cmdlet은 키 자격 증명 모음에서 키를 삭제합니다.
키가 실수로 삭제된 경우 특별한 '복구' 권한이 있는 Undo-AzKeyVaultKeyRemoval 키를 사용하여 키를 복구할 수 있습니다.
이 cmdlet은 **ConfirmImpact** 속성의 값이 높습니다.

## 예제

### 예제 1: 키 자격 증명 모음에서 키 제거
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

이 명령은 Contoso라는 키 자격 증명 모음에서 ITSoftware라는 키를 제거합니다.

### 예제 2: 사용자 확인 없이 키 제거
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

이 명령은 Contoso라는 키 자격 증명 모음에서 ITSoftware라는 키를 제거합니다.
이 명령은 *Force* 매개 변수를 지정하므로 cmdlet에서 확인 메시지를 표시하지 않습니다.

### 예제 3: 영구적으로 키 자격 증명 모음에서 삭제된 키 제거
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

이 명령은 Contoso라는 키 자격 증명 모음에서 ITSoftware라는 키를 영구적으로 제거합니다.
이 cmdlet을 실행하려면 이전에 이 키 자격 증명 모음에 대해 사용자에게 명시적으로 부여된 '제거' 권한이 필요합니다.

### 예제 4: 파이프라인 연산자를 사용하여 키 제거
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

이 명령은 Contoso라는 키 자격 증명 모음에 있는 모든 키를 사용하고 파이프라인 연산자를 사용하여 **Where-Object** cmdlet에 전달합니다.
해당 cmdlet은 **Enabled** 특성에 대한 $False 값이 있는 키를 현재 cmdlet에 전달합니다.
해당 cmdlet은 해당 키를 제거합니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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
사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.

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
HSM 이름입니다. Cmdlet은 이름 및 현재 선택한 환경에 따라 관리되는 HSM의 FQDN을 생성합니다.

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
KeyBundle 개체

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
이전에 삭제된 키를 영구적으로 제거합니다.

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

### -Name
제거할 키의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 이름, 키 자격 증명 모음의 이름 및 현재 환경에 따라 키의 FQDN(정식 도메인 이름)을 생성합니다.

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
이 cmdlet이 **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey 개체를 반환합니다.**
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

### -VaultName
키를 제거할 키 자격 증명 모음의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 이름 및 현재 환경에 따라 키 자격 증명 모음의 FQDN을 생성합니다.

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem

## 출력

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey

## 참고 사항

## 관련 링크

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)


[Undo-AzKeyVaultKeyRemoval](./Undo-AzKeyVaultKeyRemoval.md)

