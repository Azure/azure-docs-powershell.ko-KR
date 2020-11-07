---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablesastoken
schema: 2.0.0
ms.openlocfilehash: 29c5cf9b48126d4b8544cf80ad6fa78acc51ae93
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883218"
---
# New-AzureStorageTableSASToken

## SYNOPSIS
Azure 저장소 테이블에 대 한 SAS 토큰을 생성 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### SasPolicy
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SasPermission
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureStorageTableSASToken** Cmdlet은 Azure 저장소 테이블에 대 한 SAS (공유 액세스 서명) 토큰을 생성 합니다.

## 예제의

### 예제 1: 테이블에 대 한 모든 권한이 있는 SAS 토큰 생성
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

이 명령은 ContosoResources 이라는 테이블에 대 한 모든 권한이 있는 SAS 토큰을 생성 합니다.
이 토큰은 읽기, 추가, 업데이트 및 삭제 권한에 대 한 것입니다.

### 예제 2: 파티션 범위에 대 한 SAS 토큰 생성
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

이 명령은 ContosoResources 이라는 테이블에 대 한 모든 권한이 있는 SAS 토큰을 생성 합니다.
이 명령은 토큰을 *StartPartitionKey* 및 *EndPartitionKey* 매개 변수에서 지정 하는 범위로 제한 합니다.

### 예제 3: 테이블에 저장 된 액세스 정책이 있는 SAS 토큰 생성
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

이 명령은 ContosoResources 이라는 테이블에 대 한 SAS 토큰을 생성 합니다.
명령이 ClientPolicy01 이라는 저장 된 액세스 정책을 지정 합니다.

## 변수

### -컨텍스트
Azure 저장소 컨텍스트를 지정 합니다.
저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndPartitionKey
이 cmdlet이 만드는 토큰의 범위 끝에 대 한 파티션 키를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndRowKey
이 cmdlet이 만드는 토큰에 대 한 범위의 끝에 대 한 행 키를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
SAS 토큰이 만료 되는 시기를 지정 합니다.

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

### -FullUri
이 cmdlet이 SAS 토큰과 함께 전체 큐 URI를 반환 함을 나타냅니다.

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

### -IPAddressOrRange
168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.
범위는 포함입니다.

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

### -이름
Azure 저장소 테이블의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 테이블에 대 한 SAS 토큰을 만듭니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -사용 권한
Azure Storage 테이블에 대 한 사용 권한을 지정 합니다.
이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -정책
이 SAS 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.

```yaml
Type: System.String
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
* HttpsOrHttp의 기본값은 HttpsOrHttp입니다.

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartPartitionKey
이 cmdlet이 만드는 토큰에 대 한 범위의 시작에 대 한 파티션 키를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRowKey
이 cmdlet이 만드는 토큰에 대 한 범위의 시작에 대 한 행 키를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
SAS 토큰이 유효 하 게 되는 시기를 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### Microsoft. Azure. 일반. IStorageContext

## 출력

### System. 문자열

## 상속자

## 관련 링크

[새로운 AzureStorageContext](./New-AzureStorageContext.md)
