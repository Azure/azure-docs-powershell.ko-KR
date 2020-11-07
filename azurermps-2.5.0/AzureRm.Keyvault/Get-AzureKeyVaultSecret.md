---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 522268cb215a393ef54209b7606c8556d2566fd7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882238"
---
# Get-AzureKeyVaultSecret

## SYNOPSIS
키 보관소의 비밀을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByVaultName (기본값)
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretName
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretVersions
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedSecrets
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureKeyVaultSecret** cmdlet은 키 보관소의 비밀을 가져옵니다.
이 cmdlet은 키 자격 증명 모음의 특정 비밀 또는 모든 비밀을 가져옵니다.

## 예제의

### 예제 1: 키 보관소에 있는 모든 비밀에 대 한 모든 최신 버전 가져오기
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

이 명령은 Contoso 라는 키 보관소에 있는 모든 비밀의 현재 버전을 가져옵니다.

### 예제 2: 특정 비밀의 모든 버전 가져오기
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

이 명령은 Contoso 라는 키 보관소에 ITSecret 라는 모든 버전의 암호를 가져옵니다.

### 예제 3: 특정 비밀 정보의 현재 버전 가져오기
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

이 명령은 Contoso 라는 키 보관소에 ITSecret 라는 이름의 현재 버전을 가져옵니다.

### 예제 4: 특정 보안 버전 가져오기
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

이 명령은 Contoso 라는 키 보관소에 ITSecret 라는 특정 버전의 비밀을 가져옵니다.

### 예제 5: 특정 비밀의 현재 버전에 대 한 일반 텍스트 값 가져오기
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

이러한 명령은 ITSecret 라는 최신 버전의 비밀을 얻은 다음 해당 비밀의 일반 텍스트 값을 표시 합니다.

### 예제 6: 삭제 했지만이 키 보관소에는 제거 되지 않은 모든 비밀을 가져옵니다.
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 되었지만 제거 되지 않은 모든 비밀을 가져옵니다.

### 예제 7: 삭제 되었지만이 키 보관소에는 제거 되지 않은 비밀 ITSecret를 가져옵니다.
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 되었지만 제거 되지 않은 비밀 ITSecret를 가져옵니다.
이 명령은 삭제 날짜와 같은 메타 데이터를 반환 하 고, 해당 비밀의 예정 된 제거 날짜

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeVersions
이 cmdlet이 모든 보안 버전을 가져옵니다.
현재 버전의 비밀은 목록의 첫 번째입니다.
이 매개 변수를 지정 하는 경우 *Name* 및 *VaultName* 매개 변수도 지정 해야 합니다.

*Includeversions* 매개 변수를 지정 하지 않으면이 cmdlet은 지정 된 *이름을* 사용 하 여 현재 버전의 암호를 가져옵니다.

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
이전에 삭제 한 비밀을 출력에 표시할지 여부를 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
가져올 비밀의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
비밀이 속한 키 보관소의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 보관소의 FQDN (정규화 된 도메인 이름)을 생성 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -버전
비밀 버전을 지정 합니다.
이 cmdlet은 키 보관소 이름, 현재 선택 된 환경, 비밀 이름 및 비밀 버전을 기준으로 비밀의 FQDN을 생성 합니다.

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 이름

## 출력

### <를 나열 합니다. KeyVault>, SecretIdentityItem,, DeletedSecret,<등의를 나열 합니다.>, Microsoft Azure .를 확인 하세요.-KeyVault .를 표시 합니다.

## 상속자

## 관련 링크

[제거-AzureKeyVaultSecret](./Remove-AzureKeyVaultSecret.md)

[실행 취소-AzureKeyVaultSecretRemoval](./Undo-AzureKeyVaultSecretRemoval.md)

[Set-AzureKeyVaultSecret](./Set-AzureKeyVaultSecret.md)

