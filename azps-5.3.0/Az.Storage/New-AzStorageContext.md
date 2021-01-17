---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374053"
---
# New-AzStorageContext

## SYNOPSIS
Azure Storage 컨텍스트를 만듭니다.

## 구문

### OAuthAccount(기본값)
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

## 설명
**New-AzStorageContext** cmdlet은 Azure Storage 컨텍스트를 만듭니다.
스토리지 계정 이름을 입력하는 경우 스토리지 컨텍스트의 기본 인증은 OAuth(Azure AD)입니다.
에서 Storage 서비스의 인증에 대한 세부 정보를 https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services 참조합니다.

## 예제

### 예제 1: 저장소 계정 이름 및 키를 지정하여 컨텍스트 만들기
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

이 명령은 지정된 키를 사용하는 ContosoGeneral이라는 계정에 대한 컨텍스트를 만듭니다.

### 예제 2: 연결 문자열을 지정하여 컨텍스트 만들기
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

이 명령은 ContosoGeneral 계정에 대해 지정된 연결 문자열을 기반으로 컨텍스트를 만듭니다.

### 예제 3: 익명 저장소 계정에 대한 컨텍스트 만들기
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

이 명령은 ContosoGeneral이라는 계정에 익명으로 사용하기 위한 컨텍스트를 만듭니다.
이 명령은 HTTP를 연결 프로토콜로 지정합니다.

### 예제 4: 로컬 개발 저장소 계정을 사용하여 컨텍스트 만들기
```
PS C:\>New-AzStorageContext -Local
```

이 명령은 로컬 개발 저장소 계정을 사용하여 컨텍스트를 만듭니다.
이 명령은 Local 매개 *변수를 지정합니다.*

### 예제 5: 로컬 개발자 저장소 계정에 대한 컨테이너를 얻습니다.
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

이 명령은 로컬 개발 저장소 계정을 사용하여 컨텍스트를 만든 다음 파이프라인 연산자를 사용하여 **Get-AzStorageContainer** cmdlet에 새 컨텍스트를 전달합니다.
이 명령은 로컬 개발자 스토리지 계정에 대한 Azure Storage 컨테이너를 얻습니다.

### 예제 6: 여러 컨테이너를 얻습니다.
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

첫 번째 명령은 로컬 개발 저장소 계정을 사용하여 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 01 변수에 저장합니다.
두 번째 명령은 지정된 키를 사용하는 ContosoGeneral이라는 계정에 대한 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 02 변수에 저장합니다.
마지막 명령은 **Get-AzStorageContainer를** 사용하여 $Context 01 및 $Context 02에 저장된 컨텍스트에 대한 컨테이너를 얻습니다.

### 예제 7: 엔드포인트를 사용하여 컨텍스트 만들기
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

이 명령은 지정된 스토리지 엔드포인트가 있는 Azure Storage 컨텍스트를 만듭니다.
이 명령은 지정된 키를 사용하는 ContosoGeneral이라는 계정에 대한 컨텍스트를 만듭니다.

### 예제 8: 지정된 환경을 사용하여 컨텍스트 만들기
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

이 명령은 지정된 Azure 환경이 있는 Azure 저장소 컨텍스트를 만듭니다.
이 명령은 지정된 키를 사용하는 ContosoGeneral이라는 계정에 대한 컨텍스트를 만듭니다.

### 예제 9: SAS 토큰을 사용하여 컨텍스트 만들기
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

첫 번째 명령은 ContosoMain이라는 컨테이너에 **New-AzStorageContainerSASToken** cmdlet을 사용하여 SAS 토큰을 생성한 다음, 해당 토큰을 $SasToken 변수에 저장합니다.
해당 토큰은 읽기, 추가, 업데이트 및 삭제 권한을 위한 것입니다.
두 번째 명령은 ContosoGeneral이라는 계정에 대한 컨텍스트를 만들고, 이 계정에 저장된 SAS 토큰을 $SasToken 해당 컨텍스트를 $Context 변수에 저장합니다.
마지막 명령은 컨테이너에 저장된 컨텍스트를 사용하여 ContosoMain이라는 컨테이너와 연결된 모든 blob을 $Context.

### 예제 10: OAuth 인증을 사용하여 컨텍스트 만들기
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

이 명령은 OAuth(Azure AD) 인증을 사용하여 컨텍스트를 만듭니다.

## PARAMETERS

### -Anonymous
이 cmdlet이 익명 로그온에 대한 Azure Storage 컨텍스트를 만들었다는 의미입니다.

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
Azure Storage 컨텍스트에 대한 연결 문자열을 지정합니다.

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

### -Endpoint
Azure Storage 컨텍스트에 대한 엔드포인트를 지정합니다.

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

### -Environment
Azure 환경을 지정합니다.
이 매개 변수에 허용되는 값은 AzureCloud 및 AzureChinaCloud입니다.
자세한 내용은 `Get-Help Get-AzEnvironment` .를 입력합니다.

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

### -Local
이 cmdlet이 로컬 개발 저장소 계정을 사용하여 컨텍스트를 만드는지 나타냅니다.

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

### -Protocol
전송 프로토콜(https/http).

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
컨텍스트에 대한 SAS(공유 액세스 서명) 토큰을 지정합니다.

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
Azure Storage 계정 키를 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 키에 대한 컨텍스트를 만듭니다.

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
Azure Storage 계정 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 계정에 대한 컨텍스트를 만듭니다.

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
이 cmdlet이 OAuth(Azure AD) 인증을 사용하여 Azure Storage 컨텍스트를 만들었다는 의미입니다.
다른 인증이 지정되지 않은 경우 cmdlet은 기본적으로 OAuth 인증을 사용하게 됩니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext

## 참고 사항

## 관련 링크

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[New-AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)


