---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 838fb221952a97234c31c514aa82fc30be7e2f25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537304"
---
# Get-AzureRmDataLakeAnalyticsJobPipeline

## SYNOPSIS
Data Lake Analytics 작업 파이프라인이 나 파이프라인을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 계정에 모두 (기본값)
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 특정 작업 파이프라인
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmDataLakeAnalyticsJobPipeline** 에서 지정 된 Azure Data Lake Analytics 작업 파이프라인 또는 파이프라인 목록을 가져옵니다.

## 예제의

### 예제 1: 지정 된 파이프라인 가져오기
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

이 명령은 ' contosoadla ' 계정에서 id가 ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' 인 지정 된 파이프라인을 가져옵니다.

### 예제 2: 계정에 있는 모든 파이프라인 목록 가져오기
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

이 명령은 "contosoadla" 계정의 모든 파이프라인 목록을 가져옵니다.

## 변수

### -계정
작업 파이프라인을 검색 하는 데 사용할 데이터 호수 분석 계정 이름의 이름입니다.

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

### -PipelineId
정보를 반환할 특정 작업 파이프라인의 ID입니다.

```yaml
Type: System.Guid
Parameter Sets: Specific Job Pipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -다음 시간 후에 submitted
지정 된 시간 후에만 제출 되는 작업 파이프라인 (들)을 반환 하는 선택적 필터입니다.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이전에 submitted
지정 된 시간 이전에 제출할 때만 작업 파이프라인 (들)을 반환 하는 선택적 필터입니다.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
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

### System. 문자열

### 시스템 Guid

## 출력

### DataLakeAnalytics. PSJobPipelineInformation/.

## 상속자

## 관련 링크

