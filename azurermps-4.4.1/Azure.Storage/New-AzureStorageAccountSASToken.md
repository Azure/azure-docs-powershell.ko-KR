---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 8b280a13e7eb7a2e6ea3f52b4a121f313504b2ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525851"
---
# New-AzureStorageAccountSASToken

## SYNOPSIS
계정 수준 SAS 토큰을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## 설명은
**AzureStorageSASToken** Cmdlet은 Azure 저장소 계정에 대 한 sa (계정 수준 공유 액세스 서명) 토큰을 만듭니다.

SAS 토큰을 사용 하 여 여러 서비스에 대 한 사용 권한을 위임 하거나 개체 수준 SAS 토큰과 함께 사용할 수 없는 서비스에 대 한 사용 권한을 위임할 수 있습니다.

## 예제의

### 예제 1: 모든 권한이 있는 계정 수준 SAS 토큰 만들기
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

이 명령은 모든 권한이 있는 계정 수준 SAS 토큰을 만듭니다.

### 예제 2: IP 주소 범위에 대 한 계정 수준 SAS 토큰 만들기
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

이 명령은 지정 된 IP 주소 범위의 HTTPS 전용 요청에 대 한 계정 수준 SAS 토큰을 만듭니다.

## 변수

### -컨텍스트
Azure 저장소 컨텍스트를 지정 합니다.
New-AzureStorageContext cmdlet을 사용 하 여 **Azurestoragecontext** 개체를 가져올 수 있습니다.

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
저장소 계정에 대 한 사용 권한을 지정 합니다.
사용 권한은 지정 된 리소스 종류와 일치 하는 경우에만 유효 합니다.
허용 되는 사용 권한 값에 대 한 자세한 내용은 계정 SA 만들기를 참조 하세요.https://go.microsoft.com/fwlink/?LinkId=799514

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

### -프로토콜
계정 SA로 작성 된 요청에 허용 되는 프로토콜을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- HttpsOnly
- HttpsOrHttp

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

### -ResourceType
SAS 토큰과 함께 사용할 수 있는 리소스 종류를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 않아야
- Services
- 컨트롤러
- 오브젝트가

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -서비스
서비스를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 않아야
- 블
- 파일
- 전담팀
- 테이블로

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
SA가 유효 하 게 되는 **DateTime** 개체로 시간을 지정 합니다.
**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.

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

### IStorageContext

' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.

## 출력

### System. 문자열

## 상속자

## 관련 링크

[새로운 AzureStorageBlobSASToken](./New-AzureStorageBlobSASToken.md)

[새로운 AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)

[새로운 AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)

[새로운 AzureStorageQueueSASToken](./New-AzureStorageQueueSASToken.md)

[새로운 AzureStorageShareSASToken](./New-AzureStorageShareSASToken.md)

[새로운 AzureStorageTableSASToken](./New-AzureStorageTableSASToken.md)


