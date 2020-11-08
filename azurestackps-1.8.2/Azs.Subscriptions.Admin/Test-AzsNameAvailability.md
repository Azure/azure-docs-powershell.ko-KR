---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046712"
---
# Test-AzsNameAvailability

## SYNOPSIS
지정 된 구독 리소스 종류 및 이름의 avaialbility를 반환 합니다.

## 구문과

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## 설명은
지정 된 구독 리소스 종류 및 이름의 avaialbility를 반환 합니다.

## 예제의

### --------------------------예제 1--------------------------
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

지정 된 구독 리소스 종류 및 이름의 avaialbility를 반환 합니다.

## 변수

### -이름
확인할 리소스 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
확인할 리소스 종류입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### CheckNameAvailabilityResponse. 관리자. m a. 관리

## 상속자

## 관련 링크

