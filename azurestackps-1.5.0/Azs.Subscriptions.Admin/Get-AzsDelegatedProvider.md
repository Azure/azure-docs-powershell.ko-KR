---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93522908"
---
# Get-AzsDelegatedProvider

## SYNOPSIS
DelegatedProviders 목록을 가져옵니다.

## 구문과

### 목록 (기본값)
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### 가져오기
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## 설명은
DelegatedProviders 목록을 가져옵니다.

## 예제의

### --------------------------예제 1--------------------------
```
Get-AzsDelegatedProvider
```

위임 된 공급자 목록 가져오기

### --------------------------예제 2--------------------------
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

위임 된 특정 공급자를 가져옵니다.

## 변수

### -DelegatedProviderId
DelegatedProvider 식별자입니다.

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
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

