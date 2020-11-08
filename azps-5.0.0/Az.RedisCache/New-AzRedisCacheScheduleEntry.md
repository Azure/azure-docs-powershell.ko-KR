---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: e3976c1008388c85a04715541d0d88e164a422e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215694"
---
# New-AzRedisCacheScheduleEntry

## SYNOPSIS
일정 항목을 만듭니다.

## 구문과

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzRedisCacheScheduleEntry** Cmdlet은 **PSScheduleEntry** 개체를 만듭니다.
Azure Redis 캐시 패치 예약 cmdlet (예: New-AzRedisCachePatchSchedule cmdlet)에는 일정 항목 개체가 필요 합니다.

## 예제의

### 예제 1: 주말 일정 항목 만들기
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

이 명령은 지정 된 시작 시간 및 윈도를 포함 하는 주말 일정을 나타내는 **PSScheduleEntry** 개체를 만듭니다.

## 변수

### -DayOfWeek
일정 항목에 대 한 요일을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 매일 
- 주말을 
- 월요일 
- 시간은 
- 일 
- 목요일 
- 금요일 
- 토요일 
- 나타내고

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindow
업데이트에 허용 되는 시간 창 크기를 지정 합니다.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartHourUtc
일정이 시작 되는 시간 (일)을 지정 합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
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

### System. 문자열

### 시스템. i i.

### 시스템 Null 허용 ' 1 [[System. TimeSpan, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]

## 출력

### PSScheduleEntry. 모델. m e.

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트

## 관련 링크

[Get-AzRedisCachePatchSchedule](./Get-AzRedisCachePatchSchedule.md)

[새로운 AzRedisCachePatchSchedule](./New-AzRedisCachePatchSchedule.md)

[제거-AzRedisCachePatchSchedule](./Remove-AzRedisCachePatchSchedule.md)


