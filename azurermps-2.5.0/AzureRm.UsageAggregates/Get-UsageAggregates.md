---
external help file: Microsoft.Azure.Commands.UsageAggregates.dll-Help.xml
Module Name: AzureRM
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.usageaggregates/get-usageaggregates
schema: 2.0.0
ms.openlocfilehash: 70dda4d40f517d3d7bd7a3a8d64584e74f80310a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880869"
---
# Get-UsageAggregates

## SYNOPSIS
보고 된 Azure 구독 사용량 세부 정보를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**UsageAggregates** cmdlet은 다음 속성으로 집계 된 Azure 구독 사용 데이터를 가져옵니다. 

- 사용이 보고 된 시작 시간과 종료 시간입니다.

- 집계 정밀도 (매일 또는 매시간)입니다.

- 동일한 리소스의 여러 인스턴스에 대 한 인스턴스 수준 세부 정보입니다.

일관적인 결과를 위해, 반환 되는 데이터는 Azure 리소스에서 사용 현황 세부 정보를 보고 한 시기를 기준으로 합니다.

자세한 내용은 https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) Microsoft 개발자 네트워크 라이브러리의 AZURE 청구 REST API 참조를 참조 하세요.

## 예제의

### 예제 1: 구독 데이터 검색
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

이 명령은 5/2/2015와 5/5/2015 사이의 구독에 대 한 보고 된 사용량 데이터를 검색 합니다.

## 변수

### -AggregationGranularity
데이터의 집계 정밀도를 지정 합니다.
유효한 값은 일일 및 매시간입니다.

기본값은 일일 값입니다.

```yaml
Type: AggregationGranularity
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
이전 호출의 응답 본문에서 검색 한 연속 토큰을 지정 합니다.
큰 결과 집합의 경우 연속 토큰을 사용 하 여 응답을 페이징할 수 있습니다.
연속 토큰은 진행률에 대 한 책갈피 역할을 합니다.
이 매개 변수를 지정 하지 않으면 데이터는 *ReportedStartTime* 에 지정 된 일 또는 시간의 시작 부분에서 검색 됩니다.
응답에서 다음 링크를 통해 데이터 페이지를 참조 하는 것이 좋습니다.

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportedEndTime
Azure 청구 시스템에 리소스 사용이 기록 된 시점에 대해 보고 된 종료 시간을 지정 합니다.

Azure는 전세계 여러 데이터 센터에 걸친 분산 시스템 이므로 리소스가 실제로 소모 된 시기 (리소스 사용 시간)와 사용 이벤트가 청구 시스템에 도달 했을 때 리소스 사용이 보고 된 시간 사이에는 지연이 있습니다.
특정 기간 동안 보고 되는 구독에 대 한 모든 사용 이벤트를 가져오려면 보고 된 시간을 쿼리 합니다.
보고 된 시간을 기준으로 쿼리 하는 경우에도 cmdlet은 리소스 사용 시간을 기준으로 응답 데이터를 집계 합니다.
리소스 사용 데이터는 데이터 분석에 유용한 피벗입니다.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportedStartTime
Azure 청구 시스템에서 리소스 사용이 기록 된 시점에 대해 보고 된 시작 시간을 지정 합니다.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowDetails
이 cmdlet이 사용 데이터와 함께 인스턴스 수준의 세부 정보를 반환 하는지 여부를 나타냅니다.

기본값은 $True입니다.

$False 경우 서비스는 서버 쪽에서 결과를 집계 하므로 집계 그룹을 더 적게 반환 합니다.
예를 들어 세 개의 웹 사이트를 실행 하는 경우 기본적으로 웹 사이트를 사용 하는 세 개의 회선 항목이 표시 됩니다.
그러나 값이 $False 되 면 동일한 **subscriptionId** , **meterId** , **usageStartTime** 및 **usageEndTime** 에 대 한 모든 데이터가 단일 줄 항목으로 축소 됩니다.

```yaml
Type: Boolean
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

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### Microsoft UsageAggregates. UsageAggregationGetResponse.

## 상속자

## 관련 링크

