---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3874c581d1d030f9c0b77abe82b5a5a289d8960d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93874963"
---
# Get-AzsSubscriptionsQuota

## SYNOPSIS
위치에서 구독 리소스 공급자 할당량 목록을 가져옵니다.

## 구문과

### 목록 (기본값)
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### 가져오기
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### 리소스
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## 설명은
위치에서 할당량 목록 가져오기

## 예제의

### --------------------------예제 1--------------------------
```
Get-AzsSubscriptionsQuota
```

위치에서 구독 리소스 공급자 할당량 목록을 가져옵니다.

## 변수

### -위치
AzureStack 위치입니다.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
할당량의 이름입니다.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
리소스 id입니다.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### Microsoft AzureStack. 관리자. i a 관리. 할당량

## 상속자

## 관련 링크

