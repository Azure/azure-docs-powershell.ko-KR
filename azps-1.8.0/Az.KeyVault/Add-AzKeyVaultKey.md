---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: bb96183d5b1fb9b865bb4d30448c337ab58fbb09
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400589"
---
# Add-AzKeyVaultKey

## SYNOPSIS
키 자격 증명 모음에 키를 생성하거나 키를 키 자격 증명 모음으로 가져올 수 있습니다.

## 구문

### InteractiveCreate(기본값)
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InteractiveImport
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectCreate
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectImport
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdCreate
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdImport
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Add-AzKeyVaultKey** cmdlet은 Azure Key Vault의 키 자격 증명 모음에 키를 만들거나 키를 키 자격 증명 모음으로 가져올 수 있습니다.
이 cmdlet을 사용하여 다음 방법 중 원하는 방법으로 키를 추가합니다.
- Key Vault 서비스의 HSM(하드웨어 보안 모듈)에서 키를 생성합니다.
- Key Vault 서비스에서 소프트웨어에 키를 만들 수 있습니다.
- 사용자 자신의 HSM(하드웨어 보안 모듈)에서 Key Vault 서비스의 HSM으로 키를 가져올 수 있습니다.
- 컴퓨터의 .pfx 파일에서 키를 가져올 수 있습니다.
- 컴퓨터의 .pfx 파일에서 Key Vault 서비스의 HSM(하드웨어 보안 모듈)으로 키를 가져올 수 있습니다.
이러한 작업의 경우 키 특성을 제공하거나 기본 설정을 수락할 수 있습니다.
키 자격 증명 모음의 기존 키와 이름이 같은 키를 만들거나 가져오는 경우 원래 키가 새 키에 대해 지정한 값으로 업데이트됩니다. 해당 버전의 키에 대한 버전별 URI를 사용하여 이전 값에 액세스할 수 있습니다. 키 버전 및 URI 구조에 [](https://go.microsoft.com/fwlink/?linkid=518560) 대한 자세한 내용은 Key Vault REST API 설명서의 키 및 비밀 정보를 참조하세요.
참고: 자체 하드웨어 보안 모듈에서 키를 가져오기 위해 먼저 Azure Key Vault BYOK 도구 모음을 사용하여 BYOK 패키지(.byok 파일 이름 확장명을 사용하는 파일)를 생성해야 합니다. 자세한 내용은 Azure Key Vault에 대한 HSM-Protected 키를 생성하고 [전송하는 방법을 참조하세요.](https://go.microsoft.com/fwlink/?LinkId=522252)
키가 만들어지거나 업데이트된 후 cmdlet을 사용하여 키를 백업하는 Backup-AzKeyVaultKey 합니다. 삭제되지 않은 기능은 없습니다. 따라서 키를 실수로 삭제하거나 삭제한 다음 마음이 바뀌면 복원할 수 있는 백업이 없는 한 키를 복구할 수 없습니다.

## 예제

### 예제 1: 키 만들기
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

이 명령은 Contoso라는 키 자격 증명 모음에 ITSoftware라는 소프트웨어 보호 키를 만듭니다.

### 예제 2: HSM 보호 키 만들기
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

이 명령은 Contoso라는 키 자격 증명 모음에 HSM으로 보호된 키를 만듭니다.

### 예제 3: 기본값이 아닌 키 만들기
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

첫 번째 명령은 암호 해독 값을 저장하고 $KeyOperations 변수에 저장합니다.
두 번째 명령은 **Get-Date** cmdlet을 사용하여 UTC로 정의된 **DateTime** 개체를 만듭니다.
해당 개체는 향후 2년의 시간을 지정합니다. 이 명령은 이 날짜를 $Expires 저장합니다. 자세한 내용은 `Get-Help Get-Date` .를 입력합니다.
세 번째 명령은 **Get-Date** cmdlet을 사용하여 **DateTime** 개체를 만듭니다. 해당 개체는 현재 UTC 시간을 지정합니다. 이 명령은 이 날짜를 $NotBefore 저장합니다.
마지막 명령은 HSM 보호 키인 ITHsmNonDefault라는 키를 만듭니다. 이 명령은 저장된 허용되는 키 작업에 대한 값을 $KeyOperations. 이 명령은 이전 명령에서 만든 *Expires* 및 *NotBefore* 매개 변수의 시간 및 높은 심각도 및 IT에 대한 태그를 지정합니다. 새 키를 사용할 수 없습니다. **Set-AzKeyVaultKey** cmdlet을 사용하여 사용하도록 설정할 수 있습니다.

### 예제 4: HSM 보호 키 가져오기
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

이 명령은 *KeyFilePath* 매개 변수가 지정하는 위치에서 ITByok이라는 키를 가져올 수 있습니다. 가져온 키는 HSM 보호 키입니다.
자체 하드웨어 보안 모듈에서 키를 가져오기 위해 먼저 Azure Key Vault BYOK 도구 모음을 사용하여 BYOK 패키지(.byok 파일 이름 확장명을 사용하는 파일)를 생성해야 합니다.
자세한 내용은 Azure Key Vault에 대한 HSM-Protected 키를 생성하고 [전송하는 방법을 참조하세요.](https://go.microsoft.com/fwlink/?LinkId=522252)

### 예제 5: 소프트웨어로 보호된 키 가져오기
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용하여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Password 변수에 저장합니다. 자세한 내용은 `Get-Help
ConvertTo-SecureString` .를 입력합니다.
두 번째 명령은 Contoso 키 자격 증명 모음에 소프트웨어 암호를 만듭니다. 이 명령은 키의 위치와 키에 저장된 암호를 $Password.

### 예제 6: 키 가져오기 및 특성 할당
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용하여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Password 변수에 저장합니다.
두 번째 명령은 **Get-Date** cmdlet을 사용하여 **DateTime** 개체를 만든 다음 해당 개체를 $Expires 변수에 저장합니다.
세 번째 명령은 심각도 $tags 및 IT에 대한 태그를 설정하는 $tags 변수를 만듭니다.
마지막 명령은 지정된 위치에서 키를 HSM 키로 가져오습니다. 이 명령은 $Expires 저장된 만료 시간 및 $Password 암호를 지정하고 $tags.

## PARAMETERS

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

### -Destination
Key Vault 서비스에서 소프트웨어 보호 키 또는 HSM 보호 키로 키를 추가할지 여부를 지정합니다.
유효한 값은 HSM 및 Software입니다.
참고: HSM을 대상으로 사용하려면 HSM을 지원하는 키 자격 증명 모음이 있어야 합니다. Azure Key Vault의 서비스 계층 및 기능에 대한 자세한 내용은 Azure Key Vault 가격 책정 웹 사이트를 [참조하세요.](https://go.microsoft.com/fwlink/?linkid=512521)
이 매개 변수는 새 키를 만들 때 필요합니다. *KeyFilePath* 매개 변수를 사용하여 키를 가져오는 경우 이 매개 변수는 선택 사항입니다.
- 이 매개 변수를 지정하지 않으면 이 cmdlet은 .byok 파일 이름 확장명을 사용하는 키를 가져오면 해당 키를 HSM 보호 키로 가져오게 됩니다. cmdlet은 소프트웨어 보호 키로 이 키를 가져올 수 없습니다.
- 이 매개 변수를 지정하지 않으면 이 cmdlet은 .pfx 파일 이름 확장명을 사용하는 키를 가져오면 소프트웨어 보호 키로 키를 가져오게 됩니다.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disable
추가하는 키가 초기 비활성화 상태로 설정되어 있습니다. 키를 사용하려고 하면 실패합니다. 나중에 사용하도록 설정하려는 키를 미리 로드하는 경우 이 매개 변수를 사용합니다.

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
이 cmdlet에서 추가하는 키에 대한 만료 시간을 **DateTime** 개체로 지정합니다. 이 매개 변수는 UTC(협정 세계시)를 사용합니다. **DateTime 개체를** 얻습니다. **Get-Date** cmdlet을 사용합니다. 자세한 내용은 `Get-Help Get-Date` .를 입력합니다. 이 매개 변수를 지정하지 않으면 키가 만료되지 않습니다.

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
자격 증명 모음 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyFilePassword
가져온 파일의 암호를 **SecureString** 개체로 지정합니다. **SecureString** 개체를 얻습니다. **ConvertTo-SecureString** cmdlet을 사용합니다. 자세한 내용은 `Get-Help ConvertTo-SecureString` .를 입력합니다. .pfx 파일 이름 확장명을 사용하여 파일을 가져오기 위해 이 암호를 지정해야 합니다.

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyFilePath
이 cmdlet에서 가져오는 키 자료를 포함하는 로컬 파일의 경로를 지정합니다.
유효한 파일 이름 확장명은 .byok 및 .pfx입니다.
- 파일이 .byok 파일인 경우 키는 가져오기 후에 HSM에 의해 자동으로 보호되며 이 기본값을 다시 변경할 수 없습니다.
- 파일이 .pfx 파일인 경우 키를 가져온 후 소프트웨어에 의해 자동으로 보호됩니다. 이 기본값을 오버라이드하기  위해 키가 HSM으로 보호되지 있도록 대상 매개 변수를 HSM으로 설정하세요.
이 매개 변수를 지정하는 경우 *대상* 매개 변수는 선택 사항입니다.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyOps
이 cmdlet에서 추가하는 키를 사용하여 수행할 수 있는 작업의 배열을 지정합니다.
이 매개 변수를 지정하지 않으면 모든 작업을 수행할 수 있습니다.
이 매개 변수에 허용되는 값은 [JWK(JSON 웹 키)](https://go.microsoft.com/fwlink/?LinkID=613300)사양에 정의된 키 작업의 콤마로 구분된 목록입니다.
- 암호화
- 암호 해독
- 래핑
- 래프 래프 언
- 서명
- 확인

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
키 자격 증명 모음에 추가할 키의 이름을 지정합니다. 이 cmdlet은 이 매개 변수가 지정하는 이름, 키 자격 증명 모음의 이름 및 현재 환경에 따라 키의 FQDN(정식 도메인 이름)을 생성합니다. 이름은 길이가 1~63자인 문자열로, 0-9, a-z, A-Z 및 -(대시 기호)만 포함해야 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
키를 사용할 수 없는 **시간(DateTime** 개체)을 지정합니다. 이 매개 변수는 UTC를 사용합니다. **DateTime 개체를** 얻습니다. **Get-Date** cmdlet을 사용합니다. 이 매개 변수를 지정하지 않으면 키를 즉시 사용할 수 있습니다.

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

### -ResourceId
자격 증명 모음 리소스 ID입니다.

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Size
RSA 키 크기(비트)입니다. 지정하지 않으면 서비스는 안전한 기본값을 제공합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
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
이 cmdlet에서 키를 추가하는 키 자격 증명 모음의 이름을 지정합니다. 이 cmdlet은 이 매개 변수가 지정하는 이름 및 현재 환경에 따라 키 자격 증명 모음의 FQDN을 생성합니다.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

### System.String

## 출력

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey

## 참고 사항

## 관련 링크

[Backup-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

