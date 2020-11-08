---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046696"
---
# Get-AzsComputeQuota

## SYNOPSIS
계산 개체에 대 한 할당량 제한을 지정 하는 할당량을 반환 합니다.

## 구문과

### 목록 (기본값)
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### 가져오기
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### 리소스
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## 설명은
기존 할당량 목록 가져오기

## 예제의

### --------------------------예제 1--------------------------
```
Get-AzsComputeQuota -Location 'local'
```

지정 된 위치에 모든 계산 할당량을 가져옵니다.

### --------------------------예제 2--------------------------
```
Get-AzsComputeQuota 'Default Quota'
```

특정 계산 할당량을 가져옵니다.

## 변수

### -위치
{{채우기 위치 설명}}

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
할당량의 이름입니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### ComputeQuotaObject

## 상속자

## 관련 링크

