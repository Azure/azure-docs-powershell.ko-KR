---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 02e0678b9c86643df9cd4bfc2192908ed4748249
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213662"
---
# Get-AzDataLakeAnalyticsJob

## SYNOPSIS
Data Lake Analytics 작업을 가져옵니다.

## 구문과

### GetAllInResourceGroupAndAccount (기본값)
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetBySpecificJobInformation
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzDataLakeAnalyticsJob** Cmdlet은 Azure Data Lake 분석 작업을 가져옵니다.
작업을 지정 하지 않으면이 cmdlet은 모든 작업을 가져옵니다.

## 예제의

### 예제 1: 지정 된 작업 가져오기
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

이 명령은 지정 된 ID의 작업을 가져옵니다.

### 예제 2: 지난 주에 제출 된 작업 가져오기
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -포함
작업에 대해 검색할 추가 정보 유형을 나타내는 옵션을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 않아야
- DebugInfo
- 통계
- 모든

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
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
Parameter Sets: GetBySpecificJobInformation
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
Parameter Sets: GetAllInResourceGroupAndAccount
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
Parameter Sets: GetAllInResourceGroupAndAccount
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
Parameter Sets: GetAllInResourceGroupAndAccount
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
Parameter Sets: GetAllInResourceGroupAndAccount
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
Parameter Sets: GetAllInResourceGroupAndAccount
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
Parameter Sets: GetAllInResourceGroupAndAccount
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
Parameter Sets: GetAllInResourceGroupAndAccount
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
Parameter Sets: GetAllInResourceGroupAndAccount
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
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### 시스템 Guid

### DataLakeAnalytics/DataLakeAnalyticsEnums + ExtendedJobData (Microsoft.

### 시스템 Null 허용 ' 1 [[CoreLib, System.webserver, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]

### DataLake를 JobState []으로 합니다.

### DataLake의 JobResult []을 (를)

### 시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])

### 시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]

## 출력

### DataLake에 대 한 정보를 보려면

## 상속자

## 관련 링크

[중지-AzDataLakeAnalyticsJob](./Stop-AzDataLakeAnalyticsJob.md)

[제출-AzDataLakeAnalyticsJob](./Submit-AzDataLakeAnalyticsJob.md)

[Wait-AzDataLakeAnalyticsJob](./Wait-AzDataLakeAnalyticsJob.md)


