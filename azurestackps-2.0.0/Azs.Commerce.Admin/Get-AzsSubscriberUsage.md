---
external help file: ''
Module Name: Azs.Commerce.Admin
online version: https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage
schema: 2.0.0
ms.openlocfilehash: 9eed3f6f2a4d07bd48136c50ec173f801b30c928
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877208"
---
# Get-AzsSubscriberUsage

## SYNOPSIS
사용자가 UsageAggregates 하는 SubscriberUsageAggregates의 컬렉션을 가져옵니다.

## 구문과

```
Get-AzsSubscriberUsage -ReportedEndTime <DateTime> -ReportedStartTime <DateTime> [-SubscriptionId <String[]>]
 [-AggregationGranularity <String>] [-ContinuationToken <String>] [-SubscriberId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## 설명은
사용자가 UsageAggregates 하는 SubscriberUsageAggregates의 컬렉션을 가져옵니다.

## 예제의

### 예제 1: 날짜별로 집계 된 사용 현황 데이터 가져오기
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-31T00:00:00Z" -AggregationGranularity Daily
```

일일으로 집계 된 공급자에서 모든 테 넌 트에 대 한 총 30 년 12 월 2019 (UTC)에 대 한 사용량 데이터를 가져옵니다.
ReportedStartTime 및 ReportedEndTime는 일별로 반올림 해야 합니다.
서비스 관리자로 호출 하면 모든 테 넌 트에 대 한 모든 사용 데이터가 효율적으로 표시 됩니다.

### 예제 2: 시간별로 집계 한 사용량 데이터 가져오기
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-30T02:00:00Z" -AggregationGranularity Hourly
```

시간을 기준으로 집계 된 2019 년 12 월 30 일 (UTC)의 12am 사이 사용량 데이터를 가져옵니다.
ReportedStartTime 및 ReportedEndTime는 시간으로 반올림 해야 합니다.
마찬가지로 서비스 관리자로 호출 되 면 모든 테 넌 트에 대 한 모든 사용 데이터가 효율적으로 표시 됩니다.

## 변수

### -AggregationGranularity
집계 세분성입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ContinuationToken
연속 토큰입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ReportedEndTime
보고 된 종료 시간 (제외)입니다.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ReportedStartTime
보고 된 시작 시간 (포함)입니다.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriberId
테 넌 트 구독 식별자입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

## 출력

### Api20150601Preview. IUsageAggregate에 대 한 Microsoft.



## 상속자

## 관련 링크

