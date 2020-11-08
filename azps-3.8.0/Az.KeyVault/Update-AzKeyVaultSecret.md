---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034597"
---
# Update-AzKeyVaultSecret

## SYNOPSIS
키 보관소에서 비밀의 특성을 업데이트 합니다.

## 구문과

### 기본값 (기본값)
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzKeyVaultSecret** cmdlet은 키 보관소에서 비밀의 편집 가능한 특성을 업데이트 합니다.

## 예제의

### 예제 1: 비밀의 특성 수정
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

처음 네 개의 명령은 만료 날짜, NotBefore 날짜, 태그, 컨텍스트 형식에 대 한 특성을 정의 하 고 변수에 특성을 저장 합니다.
마지막 명령은 저장 된 변수를 사용 하 여 ContosoVault 이라는 키 보관소에서 HR 이라는 비밀에 대 한 특성을 수정 합니다.

### 예제 2: 비밀 태그 및 콘텐츠 형식 삭제
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

이 명령은 Contoso 라는 키 보관소에 있는 지정 된 버전의 비밀에 대 한 태그와 콘텐츠 유형을 삭제 합니다.

### 예제 3: 이름이 해당 이름으로 시작 하는 현재 버전의 비밀을 사용 하지 않도록 설정
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

첫 번째 명령은 Contoso $Vault 변수에 문자열 값을 저장 합니다.
두 번째 명령은 $Prefix 변수에 문자열 값을 저장 합니다.
세 번째 명령은 Get-AzKeyVaultSecret cmdlet을 사용 하 여 지정 된 키 보관소의 비밀을 얻은 다음 해당 비밀을 **Where-개체** cmdlet에 전달 합니다. **Where 개체** cmdlet은 해당 문자로 시작 하는 이름에 대 한 비밀 정보를 필터링 합니다. 이 명령은 필터와 일치 하는 비밀을 Update-AzKeyVaultSecret cmdlet에 연결 하 여 파이프를 비활성화 합니다.

### 예제 4: 모든 버전의 비밀에 대 한 ContentType 설정
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

처음 세 명령은 *VaultName* , *Name* , *ContentType* 매개 변수에 사용할 문자열 변수를 정의 합니다. 네 번째 명령은 Get-AzKeyVaultKey cmdlet을 사용 하 여 지정 된 키를 가져오고 Update-AzKeyVaultSecret cmdlet에 키를 파이프 하 여 콘텐츠 형식을 XML로 설정 합니다.

## 변수

### -ContentType
비밀의 콘텐츠 형식.
지정 하지 않으면 비밀의 기존 값이 변경 되지 않고 그대로 유지 됩니다.
빈 문자열을 지정 하 여 기존 콘텐츠 형식 값을 제거 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -사용
있는 경우 값이 true 이면 secret를 사용 하도록 설정 합니다.
값이 false 인 경우 비밀을 비활성화 합니다.
지정 하지 않으면 비밀의 사용/사용 안 함 상태에 대 한 기존 값이 변경 되지 않고 그대로 유지 됩니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -만료
UTC 시간에 비밀을 만료 하는 시간입니다.
지정 하지 않으면 비밀의 기존 값이 변경 되지 않고 그대로 유지 됩니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
비밀 개체

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

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
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
이전에 비밀을 사용할 수 없는 UTC 시간입니다.
지정 하지 않으면 비밀의 NotBefore 특성에 대 한 기존 값이 변경 되지 않은 상태로 유지 됩니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Cmdlet은 기본적으로 개체를 반환 하지 않습니다.
이 스위치가 지정 된 경우 비밀 개체를 반환 합니다.

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

### 태그
비밀 태그를 나타내는 해시 테이블입니다.
지정 하지 않으면 비밀의 기존 태그가 변경 되지 않은 상태로 유지 됩니다.
빈 Hashtable을 지정 하 여 태그를 제거 합니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
자격 증명 모음 이름
Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -버전
비밀 버전.
Cmdlet은 자격 증명 정보, 현재 선택 된 환경, 비밀 이름 및 비밀 버전의 비밀에 대 한 FQDN을 생성 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
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

### Microsoft. KeyVault. PSKeyVaultSecretIdentityItem

## 출력

### Microsoft. KeyVault. PSKeyVaultSecret

## 상속자

## 관련 링크
