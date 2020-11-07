---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultKeyAttribute.md
ms.openlocfilehash: df861a5efa87126b5eac1657a2b33b6fbae2110b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876688"
---
# Set-AzKeyVaultKeyAttribute

## SYNOPSIS
키 자격 증명 모음에서 키의 특성을 업데이트 합니다.

## 구문과

```
Set-AzKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzKeyVaultKeyAttribute** cmdlet은 키 자격 증명 모음에서 키의 편집 가능한 특성을 업데이트 합니다.

## 예제의

### 예제 1: 키를 수정 하 여 사용 하도록 설정 하 고 만료 날짜와 태그를 설정 합니다.
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

첫 번째 명령은 **데이터 가져오기** cmdlet을 사용 하 여 **DateTime** 개체를 만듭니다. 이 개체는 앞으로 2 년 동안 시간을 지정 합니다. 이 명령은 $Expires 변수에 해당 날짜를 저장 합니다.
자세한 내용은을 입력 `Get-Help Get-Date` 하세요.

두 번째 명령은 높은 심각도와 계정의 태그 값을 저장 하는 변수를 만듭니다.

마지막 명령은 ITSoftware 라는 키를 수정 합니다. 이 명령은 키를 설정 하 고 만료 시간을 $Expires에 저장 된 시간으로 설정 하 고 $Tags에 저장 된 태그를 설정 합니다.

### 예제 2: 모든 태그를 삭제 하는 키 수정
```
PS C:\>Set-AzKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

이 명령은 ITSoftware 라는 특정 버전의 키에 대 한 태그를 모두 삭제 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -사용
키를 사용 하거나 사용 하지 않도록 설정할지 여부를 지정 합니다. 값 $True는 키를 사용 하도록 설정 합니다. 값이 $False 키를 사용할 수 없게 합니다. 이 매개 변수를 지정 하지 않으면이 cmdlet이 키의 상태를 수정 하지 않습니다.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -만료
이 cmdlet이 업데이트 하는 키에 대 한 만료 시간을 **DateTime** 개체로 지정 합니다. 이 매개 변수는 UTC (협정 세계시)를 사용 합니다. **DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다. 자세한 내용은을 입력 `Get-Help Get-Date` 하세요.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyOps
이 cmdlet이 추가 하는 키를 사용 하 여 수행할 수 있는 작업 배열을 지정 합니다.
이 매개 변수를 지정 하지 않으면 모든 작업을 수행할 수 있습니다.

이 매개 변수에 허용 되는 값은 JSON 웹 키 사양에 정의 된 키 작업의 쉼표로 구분 된 목록입니다. 이러한 값 (대/소문자 구분)은 다음과 같습니다.

- 해독할
- 해독은
- 줄 바꿈
- 래핑을
- 등록할
- 나타나는지
- 백업할
- 복원한

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
업데이트할 키의 이름을 지정 합니다. 이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 키의 FQDN (정규화 된 도메인 이름)을 생성 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotBefore
시간을 **DateTime** 개체로 지정 하 고 그 뒤에 키를 사용할 수 없습니다.
이 매개 변수는 UTC를 사용 합니다.
**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
작업 중인 항목을 나타내는 개체를 반환 합니다.
기본적으로이 cmdlet은 출력을 생성 하지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 태그
해시 테이블 형태의 키-값 쌍입니다. 예를 들어:

@ {key0 = "value0", key1 = $null, key2 = "value2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
이 cmdlet이 키를 수정 하는 키 보관소의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.

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
키 버전을 지정 합니다.
이 cmdlet은 키 자격 증명 이름, 현재 선택 된 환경, 키 이름 및 키 버전을 기준으로 키의 FQDN을 생성 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### Microsoft. KeyVault. Keyvault

## 상속자

## 관련 링크

[추가-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[제거-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)
