---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
ms.openlocfilehash: 678453cc050ae31158f4f08e1efcda00338aca98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702670"
---
# New-AzureStorageContext

## SYNOPSIS
Azure 저장소 컨텍스트를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### AccountNameAndKey (기본값)
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### ConnectionString
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## 설명은
**새-AzureStorageContext** Cmdlet은 Azure 저장소 컨텍스트를 만듭니다.

## 예제의

### 예제 1: 저장소 계정 이름 및 키를 지정 하 여 컨텍스트 만들기
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만듭니다.

### 예제 2: 연결 문자열을 지정 하 여 컨텍스트 만들기
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

이 명령은 계정 ContosoGeneral에 대해 지정 된 연결 문자열을 기반으로 컨텍스트를 만듭니다.

### 예제 3: 익명 저장소 계정에 대 한 컨텍스트 만들기
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

이 명령은 ContosoGeneral 이라는 계정에 대 한 익명 사용을 위한 컨텍스트를 만듭니다.
명령은 HTTP를 연결 프로토콜로 지정 합니다.

### 예제 4: 로컬 개발 저장소 계정을 사용 하 여 컨텍스트 만들기
```
C:\PS>New-AzureStorageContext -Local
```

이 명령은 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만듭니다.
명령은 *Local* 매개 변수를 지정 합니다.

### 예제 5: 로컬 개발자 저장소 계정에 대 한 컨테이너 가져오기
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

이 명령은 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만든 다음 파이프라인 연산자를 사용 하 여 새 컨텍스트를 **Get-AzureStorageContainer** cmdlet에 전달 합니다.
명령은 로컬 개발자 저장소 계정에 대 한 Azure Storage 컨테이너를 가져옵니다.

### 예제 6: 여러 컨테이너 가져오기
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

첫 번째 명령은 로컬 개발 저장소 계정을 사용 하 여 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 01 변수에 저장 합니다.

두 번째 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 02 변수에 저장 합니다.

마지막 명령은 **AzureStorageContainer** 를 사용 하 여 $Context 01 및 $Context 02에 저장 된 컨텍스트의 컨테이너를 가져옵니다.

### 예제 7: 끝점을 사용 하 여 컨텍스트 만들기
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

이 명령은 지정 된 저장소 끝점을 가진 Azure 저장소 컨텍스트를 만듭니다.
이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만듭니다.

### 예제 8: 지정 된 환경을 사용 하 여 컨텍스트 만들기
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

이 명령은 지정 된 Azure environment가 있는 Azure 저장소 컨텍스트를 만듭니다.
이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만듭니다.

### 예제 9: SAS 토큰을 사용 하 여 컨텍스트 만들기
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

첫 번째 명령은 ContosoMain 이라는 컨테이너에 대 한 **New AzureStorageContainerSASToken** cmdlet을 사용 하 여 SAS 토큰을 생성 한 다음 해당 토큰을 $SasToken 변수에 저장 합니다.
이 토큰은 읽기, 추가, 업데이트 및 삭제 권한에 대 한 것입니다.

두 번째 명령은 $SasToken에 저장 된 SAS 토큰을 사용 하는 ContosoGeneral 라는 계정에 대 한 컨텍스트를 만든 다음 해당 컨텍스트를 $Context 변수에 저장 합니다.

마지막 명령은 $Context에 저장 된 컨텍스트를 사용 하 여 ContosoMain 이라는 컨테이너와 연결 된 모든 blob을 나열 합니다.

## 변수

### -익명
이 cmdlet이 익명 로그온에 대 한 Azure Storage 컨텍스트를 생성 함을 나타냅니다.

```yaml
Type: SwitchParameter
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
Type: String
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
Type: String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
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
자세한 내용은을 입력 `Get-Help Get-AzureEnvironment` 하세요.

```yaml
Type: String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SasTokenWithAzureEnvironment
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
Type: SwitchParameter
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
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
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
Type: String
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
Type: String
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
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### AzureStorageContext

## 상속자

## 관련 링크

[Get-AzureStorageBlob](./Get-AzureStorageBlob.md)

[새로운 AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)


