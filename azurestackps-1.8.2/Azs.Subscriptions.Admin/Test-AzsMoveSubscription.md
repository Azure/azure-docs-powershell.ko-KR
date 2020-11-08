---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a04836e2d361f4c9686fa5dfe62babfa57ade189
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047085"
---
# Test-AzsMoveSubscription

## SYNOPSIS
위임 된 공급자 제공 간에 사용자 구독을 이동할 수 있는지 확인 합니다.

## 구문과

```
Test-AzsMoveSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## 설명은
위임 된 공급자 제공 간에 사용자 구독을 이동할 수 있는지 확인 합니다.

## 예제의

### --------------------------예제 1--------------------------
```
Test that user subscriptions can be moved to a delegated provider offer.
```

Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"-ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

### --------------------------예제 2--------------------------
```
Test that user subscriptions can be moved from a delegated provider to the Default Provider.
```

$resourceIds = Get-AzsUserSubscription-필터 "offerName eq ' o1 '" | 선택-ExpandProperty Id Test-MoveSubscription-ResoruceId $resourceIds

## 변수

### -AsJob
이동 작업을 작업으로 실행할지 여부를 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationDelegatedProviderOffer
이 cmdlet이 구독을 이동할 정식 위임 된 공급자 제안을 지정 합니다.
구독이 기본 공급자로 다시 이동 되는 경우 NULL입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
이 cmdlet이 이동 하는 정규화 된 구독 리소스 식별자 배열을 지정 합니다.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

