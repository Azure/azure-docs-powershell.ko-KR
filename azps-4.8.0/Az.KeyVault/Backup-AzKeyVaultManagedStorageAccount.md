---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056316"
---
# Backup-AzKeyVaultManagedStorageAccount

## SYNOPSIS
KeyVault 관리 저장소 계정을 백업 합니다.

## 구문과

### ByStorageAccountName (기본값)
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByStorageAccount
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzKeyVaultManagedStorageAccount** cmdlet은 지정 된 관리 저장소 계정을 다운로드 하 고 파일에 저장 하 여 키 보관소에 백업 합니다.
다운로드 된 콘텐츠는 암호화 되어 있으므로 Azure 키 자격 증명 모음 외부에서 사용할 수 없습니다.
백업 된 저장소 계정은 백업 된 구독의 모든 키 보관소에 복원할 수 있으며,이는 보관소가 동일한 Azure 지역에 있는 경우에만 해당 됩니다.
이 cmdlet을 사용 하는 일반적인 이유는 다음과 같습니다. 
- 자격 증명 모음에서 원본을 실수로 삭제 하는 경우 저장소 계정의 오프 라인 복사본을 유지 하려고 합니다.
 
- 키 자격 증명 모음을 사용 하 여 관리 되는 저장소 계정을 만든 후 해당 개체를 다른 Azure 지역에 복제 하 여 분산 응용 프로그램의 모든 인스턴스에서 사용할 수 있도록 합니다.
**AzKeyVaultManagedStorageAccount** cmdlet을 사용 하 여 암호화 된 형식으로 관리 저장소 계정을 검색 한 다음 **Restore-AzKeyVaultManagedStorageAccount** cmdlet을 사용 하 고 두 번째 지역에서 키 자격 증명 모음을 지정 합니다.

## 예제의

### 예제 1: 자동으로 생성 된 파일 이름을 사용 하 여 관리 되는 저장소 계정 백업
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

이 명령은 MyKeyVault 이라는 키 자격 증명 모음에서 MyMSAK 이라는 관리 되는 저장소 계정을 검색 하 고, 해당 관리 저장소 계정의 백업을 자동으로 이름이 지정 된 파일에 저장 하 고, 파일 이름을 표시 합니다.

### 예제 2: 관리 저장소 계정을 지정 된 파일 이름으로 백업
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

이 명령은 MyKeyVault 이라는 키 자격 증명 모음에서 MyMSAK 이라는 관리 되는 저장소 계정을 검색 하 고, 해당 관리 되는 저장소 계정의 백업을. i a t a i a b 파일에 저장 합니다.

### 예제 3: 이전에 검색 한 관리 저장소 계정을 지정 된 파일 이름으로 백업 하 고 메시지를 표시 하지 않고 대상 파일을 덮어씁니다.
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

이 명령은 $msak 이라는 관리 되는 저장소 계정의 백업을 만듭니다. $Msak의 자격 증명 모음에 이름으로 지정 합니다. VaultName 파일에 이미 있는 경우 파일을 자동으로 덮어씁니다.

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
백업할 저장소 계정 번들은 검색 호출의 출력에서 파이프라인 됩니다.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

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
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
출력 파일입니다.
저장소 계정 백업을 저장할 출력 파일입니다.
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
Parameter Sets: ByStorageAccountName
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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### Microsoft. KeyVault. PSKeyVaultManagedStorageAccountIdentityItem

## 출력

### System. 문자열

## 상속자

## 관련 링크
