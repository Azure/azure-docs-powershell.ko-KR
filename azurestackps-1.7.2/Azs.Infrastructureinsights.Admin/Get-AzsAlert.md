---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fbec7ec2f8bcfc0d7595658f84866cf449d3e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874487"
---
# Get-AzsAlert

## SYNOPSIS
지정 된 위치에 있는 모든 알림 목록을 반환 합니다.

## 구문과

### 목록 (기본값)
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### 가져오기
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### 리소스
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## 설명은
지정 된 위치에 있는 모든 알림 목록을 반환 합니다.

## 예제의

### --------------------------예제 1--------------------------
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

이름으로 알림을 받습니다.

### --------------------------예제 2--------------------------
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

모든 활성 알림을 받고 해당 오류 및 직함을 표시 합니다.

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

### -위치
위치의 이름입니다.

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
경고 식별자입니다.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스가 있는 리소스 그룹 이름입니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### InfrastructureInsights. Alert (관리자 용)

## 상속자

## 관련 링크

