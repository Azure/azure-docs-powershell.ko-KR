---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523236"
---
# Get-AzsUserSubscription

## SYNOPSIS
사용자 구독 목록을 교환원으로 가져옵니다.

## 구문과

### 목록 (기본값)
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### 가져오기
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## 설명은
사용자 구독 목록을 교환원으로 가져옵니다.

## 예제의

### --------------------------예제 1--------------------------
```
Get-AzsUserSubscription
```

사용자 구독 목록을 교환원으로 가져옵니다.

## 변수

### -필터
OData 필터 매개 변수입니다.

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
구독 Id 매개 변수입니다.

```yaml
Type: Guid
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### Microsoft AzureStack. 관리. 구독

## 상속자

## 관련 링크

