---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 6a172de918e8b0675abaf01edf2ec198dae75b5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537308"
---
# Get-AzureRmDataLakeAnalyticsJob

## SYNOPSIS
Data Lake Analytics 작업을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 리소스 그룹 및 계정에서 모두 (기본값)
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 특정 JobInformation
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmDataLakeAnalyticsJob** Cmdlet은 Azure Data Lake 분석 작업을 가져옵니다.
작업을 지정 하지 않으면이 cmdlet은 모든 작업을 가져옵니다.

## 예제의

### 예제 1: 지정 된 작업 가져오기
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

이 명령은 지정 된 ID의 작업을 가져옵니다.

### 예제 2: 지난 주에 제출 된 작업 가져오기
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

이 명령은 지난 주에 제출 된 작업을 가져옵니다.

## 변수

### -계정
Data Lake Analytics 계정의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -포함
작업에 대해 검색할 추가 정보 유형을 나타내는 옵션을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 않아야
- DebugInfo
- 통계
- 모든

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: Specific JobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobId
가져올 작업의 ID를 지정 합니다.

```yaml
Type: System.Guid
Parameter Sets: Specific JobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -이름
작업 목록 결과를 필터링 하는 데 사용할 이름을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 않아야
- DebugInfo
- 통계
- 모든

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PipelineId
지정 된 파이프라인의 작업 부분만 반환 해야 함을 나타내는 선택적 ID입니다.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecurrenceId
지정 된 되풀이의 작업 부분만 반환 해야 하는 선택적 ID입니다.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -결과
작업 결과에 대 한 결과 필터를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 않아야
- 되었습니다
- 못함
- 했음을

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -상태
작업 결과에 대 한 상태 필터를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 들였습니다
- 새로운
- 컴파일에
- 일정
- 시킵니다
- 시작
- 정지
- 실행
- 종료

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -다음 시간 후에 submitted
날짜 필터를 지정 합니다.
이 매개 변수를 사용 하 여 작업 목록 결과를 지정 된 날짜 이후에 제출한 작업으로 필터링 합니다.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이전에 submitted
날짜 필터를 지정 합니다.
이 매개 변수를 사용 하 여 작업 목록 결과를 지정 된 날짜 이전에 제출한 작업으로 필터링 합니다.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -제출자
사용자의 전자 메일 주소를 지정 합니다.
이 매개 변수를 사용 하 여 작업 목록 결과를 지정 된 사용자가 제출한 작업으로 필터링 합니다.

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -위쪽
반환할 작업의 수를 나타내는 선택적 값입니다. 기본값은 500입니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Shap
' JobId ' 매개 변수는 파이프라인에서 ' Guid ' 형식의 값을 허용 합니다.

## 출력

### JobInformation
지정 된 작업 정보 세부 정보

### 목록<JobInformation>
지정 된 Data Lake Analytics 계정의 작업 목록입니다.

## 상속자

## 관련 링크

[중지-AzureRmDataLakeAnalyticsJob](./Stop-AzureRmDataLakeAnalyticsJob.md)

[제출-AzureRmDataLakeAnalyticsJob](./Submit-AzureRmDataLakeAnalyticsJob.md)

[Wait-AzureRmDataLakeAnalyticsJob](./Wait-AzureRmDataLakeAnalyticsJob.md)


