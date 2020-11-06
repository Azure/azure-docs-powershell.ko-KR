---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 0673b0c98e263a0c947fa984267e0eb49ccf9f9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533744"
---
# New-AzureRmBackupRetentionPolicyObject

## SYNOPSIS
백업 보존 정책을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### DailyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Monthly Yformatoneset
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MonthlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInDailyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**새 AzureRmBackupRetentionPolicyObject** Cmdlet은 Azure 백업 보존 정책을 만듭니다.
보존 정책은 백업이 얼마나 오래 복구 지점을 유지 하는 정도를 정의 합니다.
보존 유형은 다음과 같습니다. 

- Daily 
- 매주 
- 월간 
- 연도별 

사용할 각 보존 유형에 대해 하나의 보존 정책을 만듭니다.

백업 정책은 하나 이상의 보존 정책에 연결 됩니다.
백업 정책을 만들려면 New-AzureRmBackupProtectionPolicy cmdlet을 사용 합니다.
대신 Enable-AzureRmBackupProtection cmdlet에 보존 정책을 제공할 수 있습니다.

## 예제의

### 예제 1: 일일 보존을 위한 보존 정책 만들기
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

첫 번째 명령은 일일 보존 기간에 30 일간 보존 정책을 만든 다음 $Daily 변수에 저장 합니다.

두 번째 명령은 $Daily의 내용을 표시 합니다.

### 예제 2: 월 보존 정책 만들기
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

첫 번째 명령은 12 개월 동안 각 월의 10 번째 백업을 유지 하는 보존 정책을 만듭니다.
명령은 보존 정책을 $Monthly 변수에 저장 합니다.

두 번째 명령은 $Monthly의 내용을 표시 합니다.

## 변수

### -DailyRetention
이 cmdlet이 일일 보존 정책을 생성 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfMonth
백업 보존 기간을 식별 하는 월의 날짜와 기간을 지정 합니다.
이 매개 변수에 허용 되는 값은 1부터 28 까지의 정수입니다.
*DailyRetention* , *monthlyYearlyRetentionInDailyFormat, onind보조 Yformat* 및 *YearlyRetentionInDailyFormat* 매개 변수를 지정 하는 경우이 매개 변수를 지정 합니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases: 
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfWeek
요일의 배열을 지정 합니다.
이 cmdlet이 지정 하는 날짜는 백업이 보존 하는 복구 지점 및 기간을 식별 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 월요일 
- 시간은 
- 일 
- 목요일 
- 금요일 
- 토요일 
- 나타내고

*WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* 및 *YearlyRetentionInWeeklyFormat* 매개 변수를 지정 하는 경우이 매개 변수를 지정 합니다.

백업 및 보존을 위해 선택한 요일이 정렬 되어 있는지 확인 합니다.
예를 들어, 백업이 토요일에 설정 된 경우 보존 정책에도 토요일을 사용 해야 합니다.

```yaml
Type: String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -Monthly Yonindformat
이 cmdlet이 일일 형식으로 월 정책을 생성 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthlyRetentionInWeeklyFormat
이 cmdlet이 주간 형식으로 월 단위 정책을 만드는 것을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthsOfYear
해당 연도의 월 중 백업을 연간 기준으로 유지 하는 복구 지점이 있는 개월 수를 지정 합니다.
이 매개 변수에 허용 되는 값은: 1 월 또는 2 월 등의 월 이름입니다.

```yaml
Type: String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -보존
백업 지점을 저장할 보존 기간을 일, 월 또는 년 단위로 지정 합니다.
단위는이 cmdlet이 매일, 매월 또는 매년 보존 옵션을 선택 하는지 여부에 따라 달라 집니다.
예를 들어 *DailyRetention* 매개 변수를 지정 하는 경우 cmdlet은 현재 매개 변수를 일 수로 해석 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WeeklyRetention
이 cmdlet이 주간 보존 정책을 생성 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WeekNumber
백업 보존 기간을 식별 하는 월의 주를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 기본 
- 두번째 
- 제 3 
- 커피 
- 마지막

```yaml
Type: String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -YearlyRetentionInDailyFormat
이 cmdlet이 일일 형식으로 연간 보존 정책을 생성 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -YearlyRetentionInWeeklyFormat
이 cmdlet이 주간 형식으로 연간 보존 정책을 생성 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
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

## 출력

### AzureRmBackupRetentionPolicy

## 상속자
* 않아야

## 관련 링크

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[새로운 AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


