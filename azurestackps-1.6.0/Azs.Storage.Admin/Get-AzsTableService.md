---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 01b3c055873276a265859683e07cd9150ffedafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523479"
---
# Get-AzsTableService

## SYNOPSIS
테이블 서비스를 반환 합니다.

## 구문과

```
Get-AzsTableService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## 설명은
테이블 서비스를 반환 합니다.

## 예제의

### --------------------------예제 1--------------------------
```
Get-AzsTableService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

테이블 servie를 가져옵니다.

## 변수

### -FarmName
팜 Id입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
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

### TableService. 관리자. m a 관리

## 상속자

## 관련 링크

