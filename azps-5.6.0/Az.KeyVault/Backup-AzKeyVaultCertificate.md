---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: e4692d9b623ce285a2be50d51a450fd8da39a5ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968960"
---
# Backup-AzKeyVaultCertificate

## SYNOPSIS
키 자격 증명 모음에 인증서를 백업합니다.

## 구문

### ByCertificateName(기본값)
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCertificate
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Backup-AzKeyVaultCertificate** cmdlet은 키 자격 증명 모음에 지정된 인증서를 다운로드하고 파일에 저장하여 백업합니다.
인증서에 여러 버전이 있는 경우 모든 버전이 백업에 포함됩니다.
다운로드한 콘텐츠는 암호화되어 있기 때문에 Azure Key Vault 외부에서 사용할 수 없습니다.
자격 증명 모음이 동일한 Azure 지리에 있는 경우 백업된 인증서를 백업된 구독의 모든 키 자격 증명 모음에 복원할 수 있습니다.
이 cmdlet을 사용하는 일반적인 이유는 다음입니다. 
- 자격 증명 모음에서 실수로 원본을 삭제하는 경우 인증서의 오프라인 복사본을 유지하려는 경우.
 
- Key Vault를 사용하여 인증서를 만들었다가 이제 개체를 다른 Azure 지역으로 복제하여 분산된 애플리케이션의 모든 인스턴스에서 사용할 수 있습니다.
**Backup-AzKeyVaultCertificate** cmdlet을 사용하여 암호화된 형식으로 인증서를 검색한 다음 **Restore-AzKeyVaultCertificate** cmdlet을 사용하여 두 번째 지역에서 키 자격 증명 모음을 지정합니다.

## 예제

### 예제 1: 자동으로 생성된 파일 이름으로 인증서 백업
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

이 명령은 MyKeyVault라는 키 자격 증명 모음에서 MyCert라는 인증서를 검색하고 해당 인증서의 백업을 자동으로 이름이 지정된 파일에 저장하고 파일 이름을 표시합니다.

### 예제 2: 지정된 파일 이름으로 인증서 백업
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

이 명령은 MyKeyVault라는 키 자격 증명 모음에서 MyCert라는 인증서를 검색하고 해당 인증서의 백업을 Backup.Blob이라는 파일에 저장합니다.

### 예제 3: 이전에 검색한 인증서를 지정된 파일 이름으로 백업하여 메시지가 표시되지 않고 대상 파일을 덮어 덮어 덮어 니다.
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

이 명령은 인증서라는 인증서의 백업을 $cert. 자격 증명 모음의 이름은 $cert. Backup.blob이라는 파일로 VaultName을 지정하여 파일이 이미 있는 경우 파일을 자동으로 덮어 덮어 봅니다.

## 매개 변수

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
해당 파일이 있는 경우 주어진 파일을 덮어 덮어 덮어

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
검색 호출의 출력에서 백업할 비밀입니다.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
비밀 이름입니다.
Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 비밀 이름의 비밀의 FQDN을 생성합니다.

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
출력 파일입니다.
인증서의 백업을 저장할 출력 파일입니다.
지정하지 않으면 기본 파일 이름이 생성됩니다.

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
자격 증명 모음 이름입니다.
Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 생성합니다.

```yaml
Type: System.String
Parameter Sets: ByCertificateName
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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem

## 출력

### System.String

## 참고 사항

## 관련 링크
