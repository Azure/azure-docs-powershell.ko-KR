---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2DEF8B3A-4E91-4D39-AD39-1871F9FECE10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a59c93c9de0d2445f2839d9a66f4750751c987f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046510"
---
# Get-AzureWebHostingPlanMetric

## SYNOPSIS
Azure 웹 사이트 호스팅 계획에 대 한 메트릭을 가져옵니다.

## 구문과

```
Get-AzureWebHostingPlanMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

**AzureWebHostingPlanMetric** cmdlet은 구독에서 Azure 웹 호스팅 계획에 대 한 메트릭을 가져옵니다.

## 예제의

### 예제 1: 인스턴스 당 수준에서 마지막 3 시간에 대 한 메트릭 가져오기
```
PS C:\> Get-AzureWebHostingPlanMetric -WebSpaceName "eastuswebspace" -StartDate (get-date).AddHours(-3) -InstanceDetails $Metrics[1].Data 

Name : CpuPercentage 
Unit : Percent 
StartTime : 8/11/2014 7:00:00 AM 
EndTime : 8/11/2014 5:00:23 PM 
TimeGrain : PT1H 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 8:00:00 AM, Total:2, Min:9, Max:0, 
Time:8/11/2014 9:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 10:00:00 AM, Total:2, Min:8, Max:0...} $metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName
 ----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 8:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 9:00:00 AM 2 9 0 1 RD00155DC24579 
8/11/2014 10:00:00 AM 2 8 0 1 RD00155DC24599 
8/11/2014 11:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 12:00:00 PM 2 6 0 1 RD00155DC24599 
8/11/2014 1:00:00 PM 2 15 0 1 RD00155DC24599 
8/11/2014 2:00:00 PM 3 21 0 1 RD00155DC24599 
8/11/2014 3:00:00 PM 2 13 0 1 RD00155DC24599 
8/11/2014 4:00:00 PM 2 14 0 1 RD00155DC24599
```

이 명령은 인스턴스 단위 수준에서 지난 3 시간 동안 웹 호스팅 계획 메트릭을 가져옵니다.

## 변수

### -EndDate
메트릭을 반환할 종료 시간을 **DateTime** 개체로 지정 합니다.
**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.
자세한 내용은을 입력 `Get-Help Get-Date` 하세요.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceDetails
이 cmdlet에 인스턴스별 수준에 대 한 세부 정보가 포함 되어 있음을 나타냅니다.
두 개 이상의 컴퓨터에서 웹 사이트 호스팅 계획이 실행 되는 경우이 cmdlet은 각 컴퓨터에 대 한 세부 정보 메트릭을 반환 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MetricNames
가져올 메트릭의 배열을 제공 합니다.
이 매개 변수에 대 한 값을 지정 하지 않으면이 cmdlet은 모든 메트릭을 가져옵니다.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
구독에 대 한 계획의 이름을 지정 합니다.
기본적으로 **Get-AzureWebHostingPlanMetric** 는 현재 구독에 있는 모든 웹 사이트를 가져옵니다.
이 매개 변수는 와일드 카드 문자를 지원 하지 않습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -시작 날짜
메트릭을 가져올 시작 시간을 **DateTime** 개체로 지정 합니다.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeGrain
메트릭을 가져올 시간 단위를 지정 합니다.
유효한 값은 다음과 같습니다. 

- PT1M (분) 
- PT1H (시간) 
- P1D (일)

기본 값은 PT1H입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WebSpaceName
구독에 있는 웹 스페이스의 이름을 지정 합니다.
기본적으로 **Get-AzureWebHostingPlanMetric** 는 현재 구독에 있는 모든 계획을 가져옵니다.
이 매개 변수는 와일드 카드 문자를 지원 하지 않습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

###  
속성 이름으로이 cmdlet에 대 한 입력을 전달할 수 있지만 값을 기준으로 하지는 않습니다.

## 출력

###  
WindowsAzure. MetricResponse에 대 한 유틸리티.

기본적으로 **Get-AzureWebHostingPlanMetric** 는 **MetricResponse** 개체의 배열을 반환 합니다.

## 상속자

## 관련 링크

[Get-AzureWebHostingPlan](./Get-AzureWebHostingPlan.md)


