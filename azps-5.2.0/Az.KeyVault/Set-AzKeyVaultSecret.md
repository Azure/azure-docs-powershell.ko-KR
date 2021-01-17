---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 0733cf722e26cb52abdb84f7917a78d088f49fd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347481"
---
# Set-AzKeyVaultSecret

## SYNOPSIS
키 자격 증명 모음에서 비밀을 생성하거나 업데이트합니다.

## 구문

### 기본값(기본값)
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Set-AzKeyVaultSecret** cmdlet은 Azure Key Vault의 키 자격 증명 모음에 비밀을 만들거나 업데이트합니다. 비밀이 없는 경우 이 cmdlet에서 만듭니다. 비밀이 이미 있는 경우 이 cmdlet은 해당 비밀의 새 버전을 만듭니다.

## 예제

### 예제 1: 기본 특성을 사용하여 비밀 값 수정
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret

Vault Name   : Contoso
Name         : ITSecret
Version      : 8b5c0cb0326e4350bd78200fac932b51
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/8b5c0cb0326e4350bd78200fac932b51
Enabled      : True
Expires      :
Not Before   :
Created      : 5/25/2018 6:39:30 PM
Updated      : 5/25/2018 6:39:30 PM
Content Type :
Tags         :
```

첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용하여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 변수에 저장합니다. 자세한 내용은 `Get-Help
ConvertTo-SecureString` .를 입력합니다.
두 번째 명령은 Contoso라는 키 자격 증명 모음에서 ITSecret이라는 비밀의 값을 수정합니다. 비밀 값은 다음 위치에 저장된 $Secret.

### 예제 2: 사용자 지정 특성을 사용하여 비밀 값 수정
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = 'true'}
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable -Tags $Tags

Vault Name   : Contoso
Name         : ITSecret
Version      : a2c150be3ea24dd6b8286986e6364851
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/a2c150be3ea24dd6b8286986e6364851
Enabled      : False
Expires      : 5/25/2020 6:40:00 PM
Not Before   : 5/25/2018 6:40:05 PM
Created      : 5/25/2018 6:41:22 PM
Updated      : 5/25/2018 6:41:22 PM
Content Type : txt
Tags         : Name      Value
               Severity  medium
               IT        true
```

첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용하여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 변수에 저장합니다. 자세한 내용은 `Get-Help
ConvertTo-SecureString` .를 입력합니다.
다음 명령은 만료 날짜, 태그 및 컨텍스트 형식에 대한 사용자 지정 특성을 정의하고 특성을 변수에 저장합니다.
마지막 명령은 이전에 변수로 지정된 값을 사용하여 Contoso라는 키 자격 증명 모음에서 ITSecret이라는 비밀의 값을 수정합니다.

## PARAMETERS

### -ContentType
비밀의 콘텐츠 형식을 지정합니다.
기존 콘텐츠 형식을 삭제하려면 빈 문자열을 지정합니다.

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

### -Disable
이 cmdlet이 비밀을 사용하지 않도록 설정하는지 나타냅니다.

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

### -Expires
이 cmdlet이 업데이트하는 비밀에 대한 만료 시간을 **DateTime** 개체로 지정합니다.
이 매개 변수는 협정 세계시(UTC)를 사용합니다. **DateTime 개체를** 얻습니다. **Get-Date** cmdlet을 사용합니다. 자세한 내용은 `Get-Help Get-Date` .를 입력합니다.

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
수정할 비밀의 이름을 지정합니다. 이 cmdlet은 이 매개 변수가 지정하는 이름, 키 자격 증명 모음의 이름 및 현재 환경에 따라 비밀의 FQDN(정식 도메인 이름)을 생성합니다.

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
비밀을 사용할 수 없는 **시간(DateTime** 개체)을 지정합니다. 이 매개 변수는 UTC를 사용합니다. **DateTime 개체를** 얻습니다. **Get-Date** cmdlet을 사용합니다.

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

### -SecretValue
비밀의 값을 **SecureString** 개체로 지정합니다. **SecureString** 개체를 얻습니다. **ConvertTo-SecureString** cmdlet을 사용합니다. 자세한 내용은 `Get-Help
ConvertTo-SecureString` .를 입력합니다.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
해시 테이블 형식의 키-값 쌍입니다. 예: @{key0="value0";key1=$null;key2="value2"}

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
이 비밀이 속한 키 자격 증명 모음의 이름을 지정합니다. 이 cmdlet은 이 매개 변수가 지정하는 이름 및 현재 환경에 따라 키 자격 증명 모음의 FQDN을 생성합니다.

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

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## 출력

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret

## 참고 사항

## 관련 링크

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)
