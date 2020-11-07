---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://go.microsoft.com/fwlink/?LinkId=690296
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
ms.openlocfilehash: c53006a4f059fe1f243d9e0bf7a4c701a4c417a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711887"
---
# Backup-AzureKeyVaultSecret

## SYNOPSIS
키 자격 증명 모음에서 비밀을 백업 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### BySecretName (기본값)
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzureKeyVaultSecret [-Secret] <Secret> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureKeyVaultSecret** cmdlet은 지정 된 비밀을 다운로드 하 고 파일에 저장 하 여 키 보관소에 백업 합니다.
여러 버전의 비밀이 있으면 백업에 모든 버전이 포함 됩니다.
다운로드 된 콘텐츠는 암호화 되어 있으므로 Azure 키 자격 증명 모음 외부에서 사용할 수 없습니다.
백업한 비밀을 백업 된 서브스크립션의 모든 키 보관소에 복원할 수 있습니다.

이 cmdlet을 사용 하는 일반적인 이유는 다음과 같습니다.

- 비밀 정보 복사본을 사용 하 여 사용자의 키 보관소에서 비밀을 실수로 삭제 한 경우 오프 라인 복사본을 사용할 수 있습니다.
- 키 자격 증명 모음에 비밀을 추가 했으며, 이제 배포 된 응용 프로그램의 모든 인스턴스에서 사용할 수 있도록 비밀을 다른 Azure 지역에 복제 하려고 합니다. Backup-AzureKeyVaultSecret cmdlet을 사용 하 여 암호화 된 형식으로 비밀을 검색 한 다음 Restore-AzureKeyVaultSecret cmdlet을 사용 하 여 두 번째 지역에서 키 자격 증명 모음을 지정 합니다. (지역은 동일한 지리에 속해야 합니다.)

## 예제의

### 예제 1: 자동으로 생성 된 파일 이름으로 비밀 백업
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

이 명령은 MyKeyVault 이라는 키 보관소에서 MySecret 라는 비밀을 검색 하 고, 해당 비밀의 백업을 자동으로 이름이 지정 된 파일에 저장 하 고 파일 이름을 표시 합니다.

### 예제 2: 지정 된 파일 이름으로 비밀을 백업 하 고 메시지를 표시 하지 않고 기존 파일을 덮어씁니다.
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

이 명령은 키 vaultnamed MyKeyVault에서 MySecret 라는 비밀을 검색 하 고 해당 비밀의 백업을 blob 라는 파일에 저장 합니다.

### 예제 3: 이전에 지정한 파일 이름으로 검색 한 비밀 정보 백업
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

이 명령은 $secret 개체의 자격 증명 모음 이름 및 이름을 사용 하 여 암호를 검색 하 고 백업본 이라는 파일에 해당 백업을 저장 합니다.

## 변수

### -Force
출력 파일 (있는 경우)을 덮어쓰기 전에 확인 메시지가 표시 됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
백업할 비밀의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputFile
백업 blob이 저장 된 출력 파일을 지정 합니다.
이 매개 변수를 지정 하지 않으면이 cmdlet은 파일 이름을 생성 합니다.
기존 출력 파일의 이름을 지정 하는 경우 작업이 완료 되지 않으며 백업 파일이 이미 존재 한다는 오류 메시지가 반환 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -비밀
이름 및 자격 증명을 백업 작업에 사용 해야 하는 개체를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.Secret
Parameter Sets: BySecret
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
백업할 비밀을 포함 하는 키 보관소의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### 이름
Cmdlet은 키의 백업이 포함 된 출력 파일의 경로를 반환 합니다.

## 상속자

## 관련 링크

[Set-AzureKeyVaultSecret](./Set-AzureKeyVaultSecret.md)

[Get-AzureKeyVaultSecret](./Get-AzureKeyVaultSecret.md)

[제거-AzureKeyVaultSecret](./Remove-AzureKeyVaultSecret.md)

[Restore-AzureKeyVaultSecret](./Restore-AzureKeyVaultSecret.md)

