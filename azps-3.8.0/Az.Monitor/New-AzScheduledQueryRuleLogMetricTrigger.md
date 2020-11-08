---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033853"
---
# New-AzScheduledQueryRuleLogMetricTrigger

## SYNOPSIS
Log 메트릭 트리거의 형식 개체를 만듭니다.

## 구문과

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
Log 메트릭 트리거의 형식 개체를 만들며, 선택 사항입니다.
메트릭 쿼리 규칙에 대 한 트리거 조건으로, 미터법 측정 유형의 경고가 필요한 경우 사용 됩니다.

## 예제의

### 예제 1
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## 변수

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

### -MetricColumn
메트릭 값이 집계 되는 열입니다.
입력의 유효성이 확인 되지 않았습니다. New-AzScheduledQueryRule가 최종적으로 호출 되 면 먼저 유효성이 검사 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MetricTriggerType
메트릭 트리거 유형입니다.
입력의 유효성이 확인 되지 않았습니다. New-AzScheduledQueryRule가 최종적으로 호출 되 면 먼저 유효성이 검사 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -임계값
메트릭 임계값 (연속, 합계)입니다.
입력의 유효성이 확인 되지 않았습니다. New-AzScheduledQueryRule가 최종적으로 호출 되 면 먼저 유효성이 검사 됩니다.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThresholdOperator
메트릭 임계값 연산자: GreaterThan, LessThan, 같음.
입력의 유효성이 확인 되지 않았습니다. New-AzScheduledQueryRule가 최종적으로 호출 되 면 먼저 유효성이 검사 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### PSScheduledQueryRuleLogMetricTrigger를 통해 출력 합니다.

## 상속자

## 관련 링크
