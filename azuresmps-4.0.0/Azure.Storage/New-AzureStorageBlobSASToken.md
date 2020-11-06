---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8d84b310a16a73456bcd519332fa76ad1a6566
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523988"
---
# New-AzureStorageBlobSASToken

## SYNOPSIS
Azure 저장소 blob에 대 한 SAS 토큰을 생성 합니다.

## 구문과

### BlobNameWithPermission (기본값)
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### BlobPipelineWithPolicy
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### BlobPipelineWithPermission
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### BlobNameWithPolicy
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## 설명은
**AzureStorageBlobSASToken** Cmdlet은 Azure storage blob에 대 한 SAS (공유 액세스 서명) 토큰을 생성 합니다.

## 예제의

### 예제 1: full blob 권한을 사용 하 여 blob SAS 토큰 생성
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

이 예제에서는 full blob 권한이 있는 blob SAS 토큰을 생성 합니다.

### 예제 2: 수명 기간 동안 blob SAS 토큰 생성
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

이 예제에서는 수명 기간 동안 blob SAS 토큰을 생성 합니다.

## 변수

### -Blob
저장소 blob 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudBlob
**CloudBlob** 개체를 지정 합니다.
**CloudBlob** 개체를 가져오려면 [Get-azurestorageblob](./Get-AzureStorageBlob.md) cmdlet을 사용 합니다.

```yaml
Type: CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -컨테이너
저장소 컨테이너 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -컨텍스트
저장소 컨텍스트를 지정 합니다.

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
공유 액세스 서명이 만료 되는 시간을 지정 합니다.

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
저장소 blob에 대 한 사용 권한을 지정 합니다.

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -정책
Azure 저장 된 액세스 정책을 지정 합니다.

```yaml
Type: String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
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

## 관련 링크

[Get-AzureStorageBlob](./Get-AzureStorageBlob.md)

[새로운 AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)
