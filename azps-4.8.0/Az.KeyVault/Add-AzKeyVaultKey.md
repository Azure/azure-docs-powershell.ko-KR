---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 8583a078e12be5da3a6bcbbe16bc3349f51b9bdb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056318"
---
# Add-AzKeyVaultKey

## SYNOPSIS
키 자격 증명 모음에 키를 만들거나 키를 키 보관소로 가져옵니다.

## 구문과

### InteractiveCreate (기본값)
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

### Resourcei//포트
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzKeyVaultKey** Cmdlet은 Azure key vault의 키 보관소에 키를 만들거나 키를 키 모음으로 가져옵니다.
이 cmdlet을 사용 하 여 다음 방법 중 하나를 사용 하 여 키를 추가 합니다.
- 키 보관소 서비스의 HSM (하드웨어 보안 모듈)에서 키를 만듭니다.
- 키 보관소 서비스의 소프트웨어에서 키를 만듭니다.
- 키 보관소 서비스의 HSM (하드웨어 보안 모듈)에서 Hsm으로 키를 가져옵니다.
- 컴퓨터의 .pfx 파일에서 키를 가져옵니다.
- 컴퓨터에 있는 .pfx 파일의 키를 키 보관소 서비스의 Hsm (하드웨어 보안 모듈)로 가져옵니다.
이러한 작업의 경우 키 특성을 제공 하거나 기본 설정을 적용할 수 있습니다.
키 자격 증명 모음의 기존 키와 같은 이름을 가진 키를 만들거나 가져오면 새 키에 대해 지정 하는 값으로 원래 키가 업데이트 됩니다. 해당 버전의 키에 대 한 버전 관련 URI를 사용 하 여 이전 값에 액세스할 수 있습니다. 주요 버전 및 URI 구조에 대 한 자세한 내용은 키 볼트 REST API 설명서의 [키 및 비밀 정보](http://go.microsoft.com/fwlink/?linkid=518560) 를 참조 하세요.
참고: 고유한 하드웨어 보안 모듈에서 키를 가져오려면 먼저 Azure Key Vault BYOK 도구 집합을 사용 하 여 BYOK 패키지 (이름 확장명을 가진 파일)를 생성 해야 합니다. 자세한 내용은 [Azure 키 보관소에 대 한 HSM-Protected 키를 생성 하 고 전송 하는 방법을](http://go.microsoft.com/fwlink/?LinkId=522252)참조 하세요.
가장 좋은 방법은 키를 만들거나 업데이트 한 후 Backup-AzKeyVaultKey cmdlet을 사용 하 여 백업 하는 것입니다. 삭제 취소 기능이 없기 때문에 실수로 키를 삭제 하거나 삭제 한 다음 생각이 바뀌면 다시 복원할 수 있는 백업을가지고 있지 않는 한 키를 복구 가능 하지 않은 것입니다.

## 예제의

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

이 명령은 Contoso 라는 키 보관소에 ITSoftware 라는 소프트웨어 보호 키를 만듭니다.

### 예제 2: HSM으로 보호 된 키 만들기
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

이 명령은 Contoso 라는 키 보관소에 HSM으로 보호 된 키를 만듭니다.

### 예제 3: 기본값이 아닌 값을 사용 하 여 키 만들기
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

첫 번째 명령은 $KeyOperations 변수의 암호를 해독 하 고 확인 하는 값을 저장 합니다.
두 번째 명령은 **데이터 가져오기** cmdlet을 사용 하 여 UTC로 정의 된 **DateTime** 개체를 만듭니다.
이 개체는 앞으로 2 년 동안 시간을 지정 합니다. 이 명령은 $Expires 변수에 해당 날짜를 저장 합니다. 자세한 내용은을 입력 `Get-Help Get-Date` 하세요.
세 번째 명령은 **데이터 가져오기** cmdlet을 사용 하 여 **DateTime** 개체를 만듭니다. 해당 개체는 현재 UTC 시간을 지정 합니다. 이 명령은 $NotBefore 변수에 해당 날짜를 저장 합니다.
마지막 명령은 HSM으로 보호 된 키 인 ITHsmNonDefault 키를 만듭니다. 명령은 $KeyOperations 저장 된 허용 키 작업에 대 한 값을 지정 합니다. 이 명령은 이전 명령에서 만든 *만료* 및 *NotBefore* 매개 변수에 대 한 시간을 지정 하 고 높은 심각도 및이에 대 한 태그를 나타냅니다. 새 키를 사용할 수 없습니다. **AzKeyVaultKey** cmdlet을 사용 하 여이 기능을 사용 하도록 설정할 수 있습니다.

### 예제 4: HSM으로 보호 된 키 가져오기
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

이 명령은 *Keyfilepath* 매개 변수에서 지정 하는 위치에서 ITByok 라는 키를 가져옵니다. 가져온 키는 HSM으로 보호 된 키입니다.
고유한 하드웨어 보안 모듈에서 키를 가져오려면 먼저 Azure Key Vault BYOK 도구 집합을 사용 하 여 BYOK 패키지 (파일 이름 확장명이. a 1)를 생성 해야 합니다.
자세한 내용은 [Azure 키 보관소에 대 한 HSM-Protected 키를 생성 하 고 전송 하는 방법을](http://go.microsoft.com/fwlink/?LinkId=522252)참조 하세요.

### 예제 5: 소프트웨어 보호 키 가져오기
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

첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Password 변수에 저장 합니다. 자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.
두 번째 명령은 Contoso 키 보관소에 소프트웨어 비밀 번호를 만듭니다. 명령은 $Password에 저장 된 키와 암호의 위치를 지정 합니다.

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

첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Password 변수에 저장 합니다.
두 번째 명령은 **가져오기-날짜** cmdlet을 사용 하 여 **DateTime** 개체를 만든 다음 해당 개체를 $Expires 변수에 저장 합니다.
세 번째 명령은 $tags 변수를 만들어 높은 심각도 및 그에 대 한 태그를 설정 합니다.
마지막 명령은 지정 된 위치에서 HSM 키로 키를 가져옵니다. 명령은 $Password에 저장 된 $Expires 및 암호에 저장 된 만료 시간을 지정 하 고 $tags에 저장 된 태그를 적용 합니다.

### 예제 7: "자체 키 가져오기" (KEK) 기능에 대 한 키 교환 키 ()를 생성 합니다.

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

키를 생성 합니다 (키 교환 키 (KEK)). KEK는 키 가져오기 작업만 있는 RSA-HSM 키 여야 합니다. 키 보관소 Premium SKU만 RSA-HSM 키를 지원 합니다.
자세한 내용은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -대상
키 자격 증명 모음 서비스에서 키를 소프트웨어 보호 키 또는 HSM로 보호 된 키로 추가할지 여부를 지정 합니다.
유효한 값은 HSM 및 소프트웨어입니다.
참고: 대상으로 HSM을 사용 하려면 Hsm을 지 원하는 키 자격 증명 모음이 있어야 합니다. Azure 키 자격 증명 모음의 서비스 계층 및 기능에 대 한 자세한 내용은 [Azure 키 보관소 가격 웹 사이트](http://go.microsoft.com/fwlink/?linkid=512521)를 참조 하세요.
이 매개 변수는 새 키를 만들 때 필요 합니다. *Keyfilepath* 매개 변수를 사용 하 여 키를 가져오는 경우이 매개 변수는 선택 사항입니다.
- 이 매개 변수를 지정 하지 않고이 cmdlet은 file 이름 확장명이 byok 인 키를 가져오면 해당 키를 HSM 보호 키로 가져옵니다. Cmdlet에서 해당 키를 소프트웨어 보호 키로 가져올 수 없습니다.
- 이 매개 변수를 지정 하지 않고이 cmdlet이 .pfx 파일 이름 확장명을 가진 키를 가져오면 해당 키를 소프트웨어 보호 키로 가져옵니다.

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
추가 하는 키가 비활성의 초기 상태로 설정 됨을 나타냅니다. 키를 사용 하려는 시도는 실패 합니다. 나중에 사용 하려는 키를 미리 로드 하는 경우이 매개 변수를 사용 합니다.

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

### -만료
이 cmdlet이 추가 하는 키에 대 한 만료 시간을 **DateTime** 개체로 지정 합니다. 이 매개 변수는 UTC (협정 세계시)를 사용 합니다. **DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다. 자세한 내용은을 입력 `Get-Help Get-Date` 하세요. 이 매개 변수를 지정 하지 않으면 키가 만료 되지 않습니다.

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
자격 증명 모음 개체.

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
가져온 파일의 암호를 **SecureString** 개체로 지정 합니다. **Securestring** 개체를 가져오려면 **ConvertTo-SecureString** cmdlet을 사용 합니다. 자세한 내용은을 입력 `Get-Help ConvertTo-SecureString` 하세요. 파일 이름 확장명이 .pfx 인 파일을 가져오려면이 암호를 지정 해야 합니다.

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
이 cmdlet이 가져오는 키 자료가 포함 된 로컬 파일의 경로를 지정 합니다.
올바른 파일 이름 확장명은 byok 및 .pfx입니다.
- 파일을 byok 파일 인 경우 가져오기 후 키가 Hsm에 의해 자동으로 보호 되며이 기본값을 재정의할 수 없습니다.
- 파일이 .pfx 파일이 면 가져오기 후 소프트웨어에 의해 키가 자동으로 보호 됩니다. 이 기본값을 재정의 하려면 키가 HSM으로 보호 되도록 *대상* 매개 변수를 hsm으로 설정 합니다.
이 매개 변수를 지정 하는 경우 *대상* 매개 변수는 선택 사항입니다.

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
이 cmdlet이 추가 하는 키를 사용 하 여 수행할 수 있는 작업 배열을 지정 합니다.
이 매개 변수를 지정 하지 않으면 모든 작업을 수행할 수 있습니다.
이 매개 변수에 허용 되는 값은 [JSON Web key (JWK) 사양](http://go.microsoft.com/fwlink/?LinkID=613300)에 정의 된 대로 쉼표로 구분 된 키 작업 목록입니다.
- 해독할
- 해독은
- wrapKey
- unwrapKey
- 등록할
- 나타나는지
- 가져오기 (KEK만 해당) (예제 7 참조)

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

### -이름
키 자격 증명 모음에 추가할 키의 이름을 지정 합니다. 이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 키의 FQDN (정규화 된 도메인 이름)을 생성 합니다. Name은 0-9, a-z, a-z 및-(대시 기호)만 포함 하는 1 ~ 63 문자 문자열 이어야 합니다.

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
시간을 **DateTime** 개체로 지정 하 고 그 뒤에 키를 사용할 수 없습니다. 이 매개 변수는 UTC를 사용 합니다. **DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다. 이 매개 변수를 지정 하지 않으면 키를 즉시 사용할 수 있습니다.

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
자격 증명 모음 리소스 Id입니다.

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

### -크기
RSA 키 크기 (비트 단위)입니다. 지정 하지 않으면 서비스에서 안전한 기본값을 제공 합니다.

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

### 태그
해시 테이블 형태의 키-값 쌍입니다. 예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}

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
이 cmdlet이 키를 추가 하는 키 보관소의 이름을 지정 합니다. 이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.

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

### Microsoft. KeyVault. 모델. PSKeyVault

### System. 문자열

## 출력

### Microsoft. KeyVault. PSKeyVaultKey

## 상속자

## 관련 링크

[백업-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[제거-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Set-AzKeyVaultKeyAttribute](./Set-AzKeyVaultKeyAttribute.md)
