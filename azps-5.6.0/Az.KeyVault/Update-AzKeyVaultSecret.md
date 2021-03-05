---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 975395c471a08eac745bd8a9ab07cec826d5c038
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976859"
---
# Update-AzKeyVaultSecret

## SYNOPSIS
키 자격 증명 모음에서 비밀의 특성을 업데이트합니다.

## 구문

### 기본값(기본값)
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

## 설명
**Update-AzKeyVaultSecret cmdlet은** 키 자격 증명 모음에서 비밀의 편집 가능한 특성을 업데이트합니다.

## 예제

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

처음 네 가지 명령은 만료 날짜, NotBefore 날짜, 태그 및 컨텍스트 형식에 대한 특성을 정의하고, 특성을 변수에 저장합니다.
최종 명령은 저장된 변수를 사용하여 ContosoVault라는 키 자격 증명 모음의 HR이라는 비밀의 특성을 수정합니다.

### 예제 2: 비밀에 대한 태그 및 콘텐츠 형식 삭제
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

이 명령은 Contoso라는 키 자격 증명 모음에서 HR이라는 비밀의 지정된 버전에 대한 태그 및 콘텐츠 형식을 삭제합니다.

### 예제 3: 이름이 IT로 시작하는 현재 버전의 비밀을 사용하지 않도록 설정
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

첫 번째 명령은 문자열 값을 Contoso 변수에 $Vault 저장합니다.
두 번째 명령은 문자열 값 IT를 $Prefix 저장합니다.
세 번째 명령은 Get-AzKeyVaultSecret cmdlet을 사용하여 지정된 키 자격 증명 모음에서 비밀을 얻은 다음 해당 비밀을 **Where-Object** cmdlet에 전달합니다. **Where-Object** cmdlet은 IT 문자로 시작하는 이름에 대한 비밀을 필터합니다. 명령은 필터와 일치하는 비밀을 Update-AzKeyVaultSecret cmdlet에 파이프합니다.

### 예제 4: 모든 버전의 비밀에 ContentType 설정
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

처음 세 명령은 *VaultName,* *Name* 및 ContentType 매개 변수에 사용할 문자열 *변수를 정의합니다.* 네 번째 명령은 Get-AzKeyVaultKey cmdlet을 사용하여 지정된 키를 얻게 하여 해당 Update-AzKeyVaultSecret cmdlet에 키를 파이프하여 해당 콘텐츠 형식을 XML로 설정합니다.

## 매개 변수

### -ContentType
비밀의 콘텐츠 형식입니다.
지정하지 않으면 비밀의 콘텐츠 형식의 기존 값은 변경되지 않습니다.
빈 문자열을 지정하여 기존 콘텐츠 형식 값을 제거합니다.

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

### -사용하도록 설정
있는 경우 값이 true이면 비밀을 사용하도록 설정합니다.
값이 false이면 비밀을 사용하지 않도록 설정합니다.
지정하지 않으면 비밀의 사용 가능/사용 안 함 상태의 기존 값은 변경되지 않습니다.

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
UTC 시간의 비밀의 만료 시간입니다.
지정하지 않으면 비밀의 만료 시간의 기존 값은 변경되지 않습니다.

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

### -Name
비밀 이름입니다.
Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 비밀 이름의 비밀의 FQDN을 생성합니다.

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
비밀을 사용할 수 없는 UTC 시간입니다.
지정하지 않으면 비밀의 NotBefore 특성의 기존 값은 변경되지 않습니다.

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
Cmdlet은 기본적으로 개체를 반환하지 않습니다.
이 스위치가 지정되어 있는 경우 비밀 개체를 반환합니다.

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

### -Tag
비밀 태그를 나타내는 해시테이블입니다.
지정하지 않으면 비밀의 기존 태그는 변경되지 않습니다.
빈 해시테이블을 지정하여 태그를 제거합니다.

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
자격 증명 모음 이름입니다.
Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 생성합니다.

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

### -Version
비밀 버전입니다.
Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경, 비밀 이름 및 비밀 버전에서 비밀의 FQDN을 생성합니다.

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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## 출력

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret

## 참고 사항

## 관련 링크
