---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7f75f07ee8f53a57cdb2e359fb4addb51b1d7f76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527936"
---
# Backup-AzureKeyVaultCertificate

## SYNOPSIS
키 자격 증명 모음에서 인증서를 백업 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByCertificateName (기본값)
```
Backup-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCertificate
```
Backup-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureKeyVaultCertificate** cmdlet은 지정 된 인증서를 다운로드 하 고 파일에 저장 하 여 키 보관소에 백업 합니다.
인증서에 여러 버전이 있으면 모든 버전이 백업에 포함 됩니다.
다운로드 된 콘텐츠는 암호화 되어 있으므로 Azure 키 자격 증명 모음 외부에서 사용할 수 없습니다.
인증서가 백업 된 구독의 모든 키 보관소 (자격 증명 모음이 동일한 Azure 지리에 있는 경우)로 복구 될 수 있습니다.
이 cmdlet을 사용 하는 일반적인 이유는 다음과 같습니다. 
- 자격 증명 모음에서 원본을 실수로 삭제 한 경우에 대비 하 여 인증서의 오프 라인 복사본을 유지 하려고 합니다.
 
- 키 자격 증명 모음을 사용 하 여 인증서를 만든 후 분산 응용 프로그램의 모든 인스턴스에서 사용할 수 있도록 개체를 다른 Azure 지역에 복제 하려고 합니다.
**AzureKeyVaultCertificate** cmdlet을 사용 하 여 암호화 된 형식으로 인증서를 검색 한 다음 **Restore-AzureKeyVaultCertificate** cmdlet을 사용 하 고 두 번째 지역에서 키 자격 증명 모음을 지정 합니다.

## 예제의

### 예제 1: 자동으로 생성 된 파일 이름으로 인증서 백업
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

이 명령은 MyKeyVault 이라는 키 자격 증명 모음에서 MyCert 이라는 인증서를 검색 하 고, 해당 인증서의 백업을 자동으로 이름이 지정 된 파일에 저장 하 고, 파일 이름을 표시 합니다.

### 예제 2: 인증서를 지정 된 파일 이름으로 백업
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

이 명령은 MyKeyVault 이라는 키 자격 증명 모음에서 MyCert 이라는 인증서를 검색 하 고 해당 인증서의 백업을 blob 라는 파일에 저장 합니다.

### 예제 3: 이전에 검색 한 인증서를 지정 된 파일 이름으로 백업 하 고 메시지를 표시 하지 않고 대상 파일을 덮어씁니다.
```powershell
PS C:\> $cert = Get-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzureKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

이 명령은 $cert 라는 인증서의 백업을 만듭니다. $Cert의 자격 증명 모음에 이름으로 지정 합니다. VaultName 파일에 이미 있는 경우 파일을 자동으로 덮어씁니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
지정 된 파일 (있는 경우)을 덮어씁니다.

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
백업할 비밀을 검색 호출의 출력에서 파이프라인으로 만듭니다.

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

### -이름
비밀 이름.
Cmdlet은 자격 증명 정보, 현재 선택 된 환경 및 비밀 이름 으로부터 비밀의 FQDN을 생성 합니다.

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
인증서 백업을 저장할 출력 파일입니다.
지정 하지 않으면 기본 파일 이름이 생성 됩니다.

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
자격 증명 모음 이름
Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft. KeyVault. PSKeyVaultCertificateIdentityItem
매개 변수: InputObject (ByValue)

## 출력

### System. 문자열

## 상속자

## 관련 링크
