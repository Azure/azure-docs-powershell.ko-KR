---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75fef110a1266ca34bef645f39a879dda4aeeda4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523755"
---
# Get-AzsPlan

## SYNOPSIS
모든 구독에 대 한 모든 계획을 나열 합니다.

## 구문과

### ListAll (기본값)
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### 가져오기
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### 목록
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### 리소스
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## 설명은
모든 구독에 대 한 모든 계획을 나열 합니다.

## 예제의

### --------------------------예제 1--------------------------
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

이 구독에서 특정 계획을 받으세요.

## 변수

### -이름
계획의 이름입니다.

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
리소스가 있는 리소스 그룹의 이름입니다.

```yaml
Type: String
Parameter Sets: Get, List
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
Parameter Sets: ListAll, List
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
Parameter Sets: ListAll, List
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

### Microsoft AzureStack. 관리자. 관리. 계획

## 상속자

## 관련 링크

