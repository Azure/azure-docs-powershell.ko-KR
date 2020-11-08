---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217168"
---
# New-AzStorageContext

## SYNOPSIS
Azure 저장소 컨텍스트를 만듭니다.

## 구문과

### OAuthAccount (기본값)
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKey
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### OAuthAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### ConnectionString
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## 설명은
**AzStorageContext** Cmdlet은 Azure 저장소 컨텍스트를 만듭니다.
저장소 컨텍스트의 기본 인증은 입력 저장소 계정 이름만을 갖는 경우 OAuth (Azure AD)입니다.
의 저장소 서비스 인증에 대 한 세부 정보를 참조 https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services 하세요.

## 예제의

### 예제 1: 저장소 계정 이름 및 키를 지정 하 여 컨텍스트 만들기
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만듭니다.

### 예제 2: 연결 문자열을 지정 하 여 컨텍스트 만들기
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

이 명령은 계정 ContosoGeneral에 대해 지정 된 연결 문자열을 기반으로 컨텍스트를 만듭니다.

### 예제 3: 익명 저장소 계정에 대 한 컨텍스트 만들기
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

이 명령은 ContosoGeneral 이라는 계정에 대 한 익명 사용을 위한 컨텍스트를 만듭니다.
명령은 HTTP를 연결 프로토콜로 지정 합니다.

### 예제 4: 로컬 개발 저장소 계정을 사용 하 여 컨텍스트 만들기
```
PS C:\>New-AzStorageContext -Local
```

이 명령은 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만듭니다.
명령은 *Local* 매개 변수를 지정 합니다.

### 예제 5: 로컬 개발자 저장소 계정에 대 한 컨테이너 가져오기
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

이 명령은 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만든 다음 파이프라인 연산자를 사용 하 여 새 컨텍스트를 **Get-AzStorageContainer** cmdlet에 전달 합니다.
명령은 로컬 개발자 저장소 계정에 대 한 Azure Storage 컨테이너를 가져옵니다.

### 예제 6: 여러 컨테이너 가져오기
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

첫 번째 명령은 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 01 변수에 저장 합니다.
두 번째 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 02 변수에 저장 합니다.
마지막 명령은 **AzStorageContainer** 를 사용 하 여 $Context 01 및 $Context 02에 저장 된 컨텍스트의 컨테이너를 가져옵니다.

### 예제 7: 끝점을 사용 하 여 컨텍스트 만들기
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

이 명령은 지정 된 저장소 끝점을 가진 Azure 저장소 컨텍스트를 만듭니다.
이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만듭니다.

### 예제 8: 지정 된 환경을 사용 하 여 컨텍스트 만들기
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

이 명령은 지정 된 Azure environment가 있는 Azure 저장소 컨텍스트를 만듭니다.
이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만듭니다.

### 예제 9: SAS 토큰을 사용 하 여 컨텍스트 만들기
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

첫 번째 명령은 ContosoMain 이라는 컨테이너에 대 한 **New AzStorageContainerSASToken** cmdlet을 사용 하 여 SAS 토큰을 생성 한 다음 해당 토큰을 $SasToken 변수에 저장 합니다.
이 토큰은 읽기, 추가, 업데이트 및 삭제 권한에 대 한 것입니다.
두 번째 명령은 $SasToken에 저장 된 SAS 토큰을 사용 하는 ContosoGeneral 라는 계정에 대 한 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 변수에 저장 합니다.
마지막 명령은 $Context에 저장 된 컨텍스트를 사용 하 여 ContosoMain 이라는 컨테이너와 연결 된 모든 blob을 나열 합니다.

### 예제 10: OAuth 인증을 사용 하 여 컨텍스트 만들기
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

이 명령은 OAuth (Azure AD) 인증을 사용 하 여 컨텍스트를 만듭니다.

## 변수

### -익명
이 cmdlet이 익명 로그온에 대 한 Azure Storage 컨텍스트를 생성 함을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Azure 저장소 컨텍스트에 대 한 연결 문자열을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -끝점
Azure 저장소 컨텍스트에 대 한 끝점을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -환경
Azure 환경을 지정 합니다.
이 매개 변수에 허용 되는 값은 AzureCloud 및 AzureChinaCloud입니다.
자세한 내용은을 입력 `Get-Help Get-AzEnvironment` 하세요.

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -로컬
이 cmdlet이 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만들기를 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로토콜
전송 프로토콜 (https/http).

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasToken
컨텍스트에 대 한 SAS (공유 액세스 서명) 토큰을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
Azure 저장소 계정 키를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 키에 대 한 컨텍스트를 만듭니다.

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Azure 저장소 계정 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 계정에 대 한 컨텍스트를 만듭니다.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseConnectedAccount
이 cmdlet이 OAuth (Azure AD) 인증을 사용 하 여 Azure Storage 컨텍스트를 생성 함을 나타냅니다.
다른 인증을 지정 하지 않은 경우 cmdlet이 기본적으로 OAuth 인증을 사용 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### WindowsAzure.-저장소. AzureStorageContext

## 상속자

## 관련 링크

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[새로운 AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)


