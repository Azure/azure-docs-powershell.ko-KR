---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045548"
---
# Get-AzureStorageKey

## SYNOPSIS
Azure 저장소 계정에 대 한 기본 및 보조 저장소 계정 키를 반환 합니다.

## 구문과

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**Get-AzureStorageKey** Cmdlet은 azure 저장소 계정 이름, 기본 계정 키, 지정 된 Azure 저장소 계정의 보조 계정 키를 포함 하는 개체를 속성으로 반환 합니다.

## 예제의

### 예제 1: 기본 및 보조 저장소 키를 포함 하는 개체 가져오기
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

이 명령은 ContosoStore01 저장소 계정에 대 한 기본 및 보조 저장소 키를 사용 하 여 개체를 가져옵니다.

### 예제 2: 기본 저장소 계정 키를 받아 변수에 저장
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

이 명령은 ContosoStore01 저장소 계정에 대 한 기본 저장소 계정 키를 $ContosoStoreKey 변수에 저장 합니다.

## 변수

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
저장소 계정 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자
* Node.js에 대 한 도움말을 보려면 `help node-dev` 명령을 사용 합니다. PHP 확장에 대 한 도움말을 보려면이 `help php-dev` 명령을 사용 합니다.

## 관련 링크

[Get-AzureStorageAccount](./Get-AzureStorageAccount.md)

[새-AzureStorageAccount](./New-AzureStorageAccount.md)

[새-AzureStorageKey](./New-AzureStorageKey.md)

[-AzureStorageAccount 제거](./Remove-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


