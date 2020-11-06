---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cf36bf232ae48891b28562313fa2063e14a2be8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523391"
---
# Get-AzsDiskMigrationJob

## SYNOPSIS
관리 되는 디스크 마이그레이션 작업의 목록을 반환 합니다.

## 구문과

### 목록 (기본값)
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### 리소스
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### 가져오기
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## 설명은
디스크 마이그레이션 작업 목록을 반환 합니다.

## 예제의

### --------------------------예제 1--------------------------
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

특정 관리 디스크 마이그레이션 작업을 가져옵니다.

### --------------------------예제 2--------------------------
```
$migration = Get-AzsDiskMigrationJob -location local
```

로컬 위치에서 관리 되는 디스크 마이그레이션 작업의 목록을 반환 합니다.

## 변수

### -위치
리소스의 위치입니다.

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
마이그레이션 작업 guid 이름입니다.

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

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
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -상태
디스크 마이그레이션 작업 상태의 매개 변수입니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### DiskMigrationJob의. 관리자. 관리.

## 상속자

## 관련 링크

