---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 268a306597fe3760e8abc7e31f980da078bf2bc2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523783"
---
# Get-AzsUpdateRun

## SYNOPSIS
업데이트 실행 목록을 가져옵니다.

## 구문과

### 목록 (기본값)
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### 가져오기
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### 리소스
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## 설명은
업데이트 실행 목록을 가져옵니다. 반환 되는 UpdateRun 개체의 인스턴스는 해당 되는 경우 다시 시작 하도록 파이프 될 수 있습니다 (AzsUpdateRun).

## 예제의

### --------------------------예제 1--------------------------
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

특정 업데이트를 적용 하기 위한 모든 시도 목록을 가져옵니다.

## 변수

### -위치
업데이트 위치의 이름입니다.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
업데이트 실행 식별자입니다.

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

### -ResourceGroupName
리소스가 있는 리소스 그룹입니다.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
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
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -생략
매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -위쪽
매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.
-Skip 매개 변수 뒤에 적용 됩니다.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateName
업데이트의 이름입니다.

```yaml
Type: String
Parameter Sets: List, Get
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

### UpdateRun. 관리자. m m/. 관리

## 상속자

## 관련 링크

