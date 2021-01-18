---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 858966f5fb20f001dc21363875362673884fcc90
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496244"
---
# Get-UsageAggregates

## SYNOPSIS
보고된 Azure 구독 사용량 세부 정보를 얻습니다.

## 구문

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-UsageAggregates** cmdlet은 다음 속성으로 집계된 Azure 구독 사용량 데이터를 얻습니다. 
- 사용량이 보고된 시작 및 종료 시간입니다.
- 집계 정밀도(매일 또는 시간당).
- 동일한 리소스의 여러 인스턴스에 대한 인스턴스 수준 세부 정보입니다.
일관된 결과를 위해 반환된 데이터는 Azure 리소스에서 사용량 세부 정보를 보고한 때를 기반으로 합니다.
자세한 내용은 Azure 청구 REST API 참조(Microsoft Developer Network https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) 참조).를 참조하세요.

## 예제

### 예제 1: 구독 데이터 검색
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

이 명령은 2015년 5월 2일에서 2015년 5월 5일 사이의 구독에 대해 보고된 사용 현황 데이터를 검색합니다.

## PARAMETERS

### -AggregationGranularity
데이터의 집계 정밀도를 지정합니다.
유효한 값은 매일 및 시간별입니다.
기본값은 매일입니다.

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinuationToken
이전 호출의 응답 본문에서 검색된 연속 토큰을 지정합니다.
큰 결과 집합의 경우 연속 토큰을 사용하여 응답을 페이지화합니다.
연속 토큰은 진행 상황을 위한 책갈피 역할을 합니다.
이 매개 변수를 지정하지 않으면 *ReportedStartTime에* 지정된 하루 또는 시간의 시작부터 데이터가 검색됩니다.
데이터를 통해 페이지에 대한 응답의 다음 링크를 따르는 것이 좋습니다.

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
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -ReportedEndTime
Azure 청구 시스템에 리소스 사용량이 기록된 시기에 대해 보고된 종료 시간을 지정합니다.
Azure는 전 세계 여러 데이터 센터에 걸쳐 있는 분산 시스템으로, 리소스가 실제로 사용된 시기, 리소스 사용 시간, 사용량 이벤트가 청구 시스템에 도달한 시간(보고된 리소스 사용 시간) 사이에 지연이 있습니다.
일정 기간 동안 보고된 구독에 대한 모든 사용 이벤트를 얻기 위해 보고된 시간으로 쿼리합니다.
보고된 시간으로 쿼리하는 경우에도 cmdlet은 리소스 사용 시간별로 응답 데이터를 집계합니다.
리소스 사용 데이터는 데이터를 분석하는 데 유용한 피벗입니다.

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
Azure 청구 시스템에 리소스 사용량이 기록된 시기에 대해 보고된 시작 시간을 지정합니다.

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

### -ShowDetails
이 cmdlet이 사용 현황 데이터와 함께 인스턴스 수준 세부 정보를 반환하는지 여부를 나타냅니다.
기본값은 $True.
이 $False 경우 서비스는 서버 쪽에서 결과를 집계하므로 더 적은 수의 집계 그룹을 반환합니다.
예를 들어 세 개의 웹 사이트를 실행하는 경우 기본적으로 웹 사이트 사용에 대한 3개의 줄 항목을 얻게 됩니다.
그러나 값이 $False 경우 동일한 **subscriptionId,** **meterId,** **usageStartTime** 및 **usageEndTime에** 대한 모든 데이터가 단일 줄 항목으로 축소됩니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse

## 참고 사항

## 관련 링크
