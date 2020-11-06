---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3251e0fabb99a9f16a497a445fa010a01187108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523556"
---
# Select-AzureRmProfile

## SYNOPSIS
파일에서 Azure 인증 정보를 로드 합니다.

## 구문과

### InMemoryProfile
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### ProfileFromDisk
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## 설명은
Select-AzureRmProfile cmdlet은 파일에서 인증 정보를 로드 하 여 Azure 환경 및 컨텍스트를 설정 합니다.
현재 세션에서 실행 하는 cmdlet은이 정보를 사용 하 여 Azure Resource Manager에 대 한 요청을 인증 합니다.

## 예제의

### 예제 1: PSAzureProfile에서 프로필 선택
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

이 예제에서는 cmdlet으로 전달 되는 PSAzureProfile의 프로필을 선택 합니다.

### 예제 2: JSON 파일에서 프로필 선택
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

이 예제에서는 cmdlet으로 전달 되는 JSON 파일에서 프로필을 선택 합니다. 이 JSON 파일은 Save-AzureRmProfile에서 만들 수 있습니다.

## 변수

### -Path
저장-AzureRMProfile를 사용 하 여 저장 된 프로필 정보의 경로를 지정 합니다.

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### PSAzureProfile

## 상속자

## 관련 링크

[Get-AzureRMContext]()

