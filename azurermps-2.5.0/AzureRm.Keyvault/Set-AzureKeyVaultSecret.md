---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 0c482d3fd4e2e02221799ea72e61eacc80ff9e2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882217"
---
# Set-AzureKeyVaultSecret

## SYNOPSIS
키 자격 증명 모음에서 비밀을 만들거나 업데이트 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureKeyVaultSecret** Cmdlet은 Azure key vault의 키 보관소에서 비밀을 만들거나 업데이트 합니다. 비밀이 존재 하지 않는 경우이 cmdlet이이를 만듭니다. 비밀이 이미 있는 경우이 cmdlet은 해당 비밀의 새 버전을 만듭니다.

## 예제의

### 예제 1: 기본 특성을 사용 하 여 비밀 값 수정
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 변수에 저장 합니다. 자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.

두 번째 명령은 Contoso 라는 이름의 자격 증명 모음에서 ITSecret 라는 비밀 키의 값을 수정 합니다. 비밀 값이 $Secret에 저장 된 값이 됩니다.

### 예제 2: 사용자 지정 특성을 사용 하 여 비밀 값 수정
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 변수에 저장 합니다. 자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.

다음 명령은 만료 날짜, 태그, 컨텍스트 형식에 대 한 사용자 지정 특성을 정의 하 고 변수에 특성을 저장 합니다.

마지막 명령은 이전에 변수로 지정 된 값을 사용 하 여 Contoso 라는 키 보관소에 ITSecret 라는 비밀 값을 수정 합니다.

## 변수

### -ContentType
비밀의 콘텐츠 유형을 지정 합니다.
기존 콘텐츠 형식을 삭제 하려면 빈 문자열을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Disable
이 cmdlet이 비밀을 사용 하지 않도록 지정 합니다.

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

### -만료
이 cmdlet이 업데이트 하는 비밀에 대 한 만료 시간을 **DateTime** 개체로 지정 합니다.
이 매개 변수는 UTC (협정 세계시)를 사용 합니다. **DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다. 자세한 내용은을 입력 `Get-Help Get-Date` 하세요.

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

### -이름
수정할 비밀의 이름을 지정 합니다. 이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 비밀의 FQDN (정규화 된 도메인 이름)을 생성 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotBefore
시간을 **DateTime** 개체로 지정 하 고 그 뒤에 비밀을 사용할 수 없습니다. 이 매개 변수는 UTC를 사용 합니다. **DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.

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

### -SecretValue
암호 값을 **SecureString** 개체로 지정 합니다. **Securestring** 개체를 가져오려면 **ConvertTo-SecureString** cmdlet을 사용 합니다. 자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
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
이 비밀이 속한 키 보관소의 이름을 지정 합니다. 이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### Microsoft. KeyVault. 모델 암호

## 상속자

## 관련 링크

[Get-AzureKeyVaultSecret](./Get-AzureKeyVaultSecret.md)

[제거-AzureKeyVaultSecret](./Remove-AzureKeyVaultSecret.md)
