---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: ''
schema: 2.0.0
ms.openlocfilehash: 427276a496108a48b69fd81cb5835d74859c25b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523564"
---
# New-AzureStorageShareSASToken

## SYNOPSIS
Azure 저장소 공유에 대 한 공유 액세스 서명 토큰을 생성 합니다.

## 구문과

### SasPolicy
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### SasPermission
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## 설명은
**AzureStorageShareSASToken** Cmdlet은 Azure 저장소 공유에 대 한 공유 액세스 서명 토큰을 생성 합니다.

## 예제의

### 예제 1: 공유에 대 한 공유 액세스 서명 토큰 생성
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

이 명령은 ContosoShare 이라는 공유에 대 한 공유 액세스 서명 토큰을 만듭니다.

### 예제 2: 파이프라인을 사용 하 여 여러 공유 액세스 서명 토큰 생성
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

이 명령은 접두사 테스트와 일치 하는 모든 저장소 공유를 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여이를 현재 cmdlet에 전달 합니다.
현재 cmdlet은 지정 된 사용 권한을 가진 각 저장소 공유에 대 한 공유 액세스 토큰을 만듭니다.

### 예제 3: 공유 액세스 정책을 사용 하는 공유 액세스 서명 토큰 생성
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

이 명령은 ContosoPolicy03 이라는 정책이 있는 ContosoShare 이라는 저장소 공유에 대 한 공유 액세스 서명 토큰을 만듭니다.

## 변수

### -컨텍스트
Azure 저장소 컨텍스트를 지정 합니다.
컨텍스트를 가져오려면 New-AzureStorageContext cmdlet을 사용 합니다.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ExpiryTime
공유 액세스 서명이 무효화 되는 시간을 지정 합니다.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullUri
이 cmdlet이 full blob URI 및 공유 액세스 서명 토큰을 반환 함을 나타냅니다.

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

### -IPAddressOrRange
168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.
범위는 포함입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -사용 권한
공유 아래에 있는 공유 및 파일에 액세스할 수 있는 토큰의 사용 권한을 지정 합니다.

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -정책
공유에 대 한 저장 된 액세스 정책을 지정 합니다.

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로토콜
요청에 허용 된 프로토콜을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
* HttpsOnly
* HttpsOrHttp

기본값은 HttpsOrHttp입니다.

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShareName
저장소 공유의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -StartTime
공유 액세스 서명이 유효 하 게 되는 시간을 지정 합니다.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

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

## 상속자
* 키워드: common, azure, services, data, 저장소, blob, 대기열, 테이블

## 관련 링크

[Get-AzureStorageShare](./Get-AzureStorageShare.md)

[새로운 AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)
