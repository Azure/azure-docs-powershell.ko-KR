---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: a171f967a937873b85adcfca732987037e6db0a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386387"
---
# Backup-AzKeyVaultSecret

## SYNOPSIS
키 자격 증명 모음에 비밀을 백업합니다.

## 구문

### BySecretName(기본값)
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Backup-AzKeyVaultSecret** cmdlet은 키 자격 증명 모음에 지정된 비밀을 다운로드하고 파일에 저장하여 백업합니다.
비밀 버전이 여러 개 있는 경우 모든 버전이 백업에 포함됩니다.
다운로드한 콘텐츠는 암호화되어 있기 때문에 Azure Key Vault 외부에서 사용할 수 없습니다.
백업된 비밀을 백업된 구독의 키 자격 증명 모음에 복원할 수 있습니다.
이 cmdlet을 사용하는 일반적인 이유는
- 키 자격 증명 모음에서 비밀을 실수로 삭제하는 경우 오프라인 복사본이 있도록 비밀의 복사본을 에코로 에코합니다.
- 키 자격 증명 모음에 비밀을 추가하고 이제 다른 Azure 지역에 비밀을 복제하여 분산된 애플리케이션의 모든 인스턴스에서 사용할 수 있도록 하려는 경우 Backup-AzKeyVaultSecret cmdlet을 사용하여 암호화된 형식으로 비밀을 검색한 다음 Restore-AzKeyVaultSecret cmdlet을 사용하여 두 번째 지역에 키 자격 증명 모음을 지정합니다. (지역은 동일한 지역에 속해야 합니다.)

## 예제

### 예제 1: 자동으로 생성된 파일 이름으로 비밀 백업
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

이 명령은 MyKeyVault라는 키 자격 증명 모음에서 MySecret이라는 비밀을 검색하고 해당 비밀의 백업을 자동으로 명명된 파일에 저장하고 파일 이름을 표시합니다.

### 예제 2: 메시지를 표시하지 않고 기존 파일을 덮어매는 지정된 파일 이름에 비밀 백업
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

이 명령은 Key Vault 이름이 MyKeyVault인 MyKeyVault에서 MySecret이라는 비밀을 검색하고 해당 비밀의 백업을 Backup.blob이라는 파일에 저장합니다.

### 예제 3: 이전에 검색된 비밀을 지정된 파일 이름으로 백업
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

이 명령은 $secret 개체의 자격 증명 모음 이름 및 이름을 사용하여 비밀을 검색하고 Backup.blob이라는 파일에 백업을 저장합니다.

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
출력 파일을 덮어 사용(있는 경우)하기 전에 확인을 요청합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
검색 호출의 출력에서 파이프라인으로 백업할 비밀입니다.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
백업할 비밀의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
백업 Blob이 저장되는 출력 파일을 지정합니다.
이 매개 변수를 지정하지 않으면 이 cmdlet에서 파일 이름을 생성합니다.
기존 출력 파일의 이름을 지정하면 작업이 완료되지 않습니다. 백업 파일이 이미 있는 오류 메시지가 반환됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
백업할 비밀을 포함하는 키 자격 증명 모음의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: BySecretName
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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## 출력

### System.String

## 참고 사항

## 관련 링크

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Restore-AzKeyVaultSecret](./Restore-AzKeyVaultSecret.md)

