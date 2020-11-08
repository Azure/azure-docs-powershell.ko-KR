---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EB4A7F84-99E4-49B1-856D-EC0736058D23
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8cab29cd7d285d2ae1aae9c007be965e1bbf8f2f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045850"
---
# Set-AzureStorageAccount

## SYNOPSIS
Azure 구독에서 저장소 계정의 속성을 업데이트 합니다.

## 구문과

### AccountType (기본값)
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### GeoReplicationEnabled
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-GeoReplicationEnabled <Boolean>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**집합-AzureStorageAccount** cmdlet은 현재 구독에서 Azure 저장소 계정의 속성을 업데이트 합니다.
설정할 수 있는 속성은 **레이블** , **설명** , **형식** 및 **GeoReplicationEnabled** 입니다.

## 예제의

### 예제 1: 저장소 계정의 레이블 업데이트
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -Label "ContosoAccnt" -Description "Contoso storage account"
```

이 명령은 ContosoStorage01 이라는 저장소 계정에 대 한 **레이블** 및 **설명** 속성을 업데이트 합니다.

### 예제 2: 저장소 계정에 대 한 지리적 복제 사용
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $False
```

이 명령은 **GeoReplicationEnabled** 속성을 ContosoStorage01 이라는 저장소 계정에 대 한 $False로 설정 합니다.

### 예제 3: 저장소 계정에 대 한 지리적 복제 비활성화
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $True
```

이 명령은 **GeoReplicationEnabled** 속성을 ContosoStorage01 이라는 저장소 계정에 대 한 $True로 설정 합니다.

## 변수

### -설명
저장소 계정에 대 한 설명을 지정 합니다.
설명은 최대 1024 자를 초과할 수 있습니다.

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

### -GeoReplicationEnabled
지리적 복제를 사용 하도록 설정 하 여 저장소 계정을 만들지 여부를 지정 합니다.

```yaml
Type: Boolean
Parameter Sets: GeoReplicationEnabled
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
정보 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -레이블
저장소 계정에 대 한 레이블을 지정 합니다.
레이블은 최대 100 자를 초과할 수 있습니다.

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

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
이 cmdlet이 수정 하는 저장소 계정의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
저장소 계정의 유형을 지정 합니다.
유효한 값은 다음과 같습니다. 

- Standard_LRS
- Standard_ZRS
- Standard_GRS
- Standard_RAGRS
- Premium_LRS

이 매개 변수를 지정 하지 않을 경우 기본값은 Standard_GRS입니다.

*GeoReplicationEnabled* 매개 변수를 지정 하는 효과는 *형식* 매개 변수에 Standard_GRS를 지정 하는 것과 같습니다.

Standard_ZRS 또는 Premium_LRS 계정은 다른 계정 유형으로 변경 하거나 그 반대의 경우도 마찬가지입니다.

```yaml
Type: String
Parameter Sets: AccountType
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

[Get-AzureStorageAccount](./Get-AzureStorageAccount.md)

[새-AzureStorageAccount](./New-AzureStorageAccount.md)

[-AzureStorageAccount 제거](./Remove-AzureStorageAccount.md)


