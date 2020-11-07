---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: b012704eebfa9d2c2a868679450cd0231667f585
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711855"
---
# Start-AzureRmStreamAnalyticsJob

## SYNOPSIS
Stream Analytics 작업을 시작 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Start-AzureRmStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmStreamAnalyticsJob** Cmdlet은 Azure에서 Stream Analytics 작업을 비동기적으로 배포 하 고 시작 합니다.

## 예제의

### 예제 1: Stream Analytics 작업 시작
```
PS C:\>Start-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

이 명령은 작업 StreamingJob을 시작 하 고 출력 이벤트 스트림이 timestamp 2014 년 1 ~ 7-03T01:00Z에 시작 되도록 지정 합니다.

## 변수

### -이름
시작할 Azure Stream Analytics 작업의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputStartMode
작업의 시작 모드를 지정 합니다.
유효한 값은 다음과 같습니다. 

- JobStartTime-이 값은 작업이 시작 될 때 출력 이벤트 스트림의 시작 지점이 시작 됨을 나타냅니다.
- CustomTime-이 값은 출력 이벤트 스트림의 시작 지점이 *OutputStartTime* 매개 변수에 지정 된 사용자 지정 시간에 시작 되어야 함을 나타냅니다. 
 --LastOutputEventTime-이 값은 출력 이벤트 스트림의 시작 지점이 마지막 이벤트 출력 시간에서 시작 해야 함을 나타냅니다.

속성이 없으면 JobStartTime입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputStartTime
출력 시작 시간을 지정 합니다.
이 값은 출력 이벤트 스트림의 시작 지점을 나타내는 ISO 8601 형식 지정 된 타임 스탬프 이거나, 스트리밍 작업이 시작 될 때마다 출력 이벤트 스트림이 시작 됨을 나타내는 $Null입니다.
*OutputStartMode* 가 customtime으로 설정 된 경우이 속성에 값이 있어야 합니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

## 출력

### System. 개체

## 상속자

## 관련 링크

[Get-AzureRmStreamAnalyticsJob](./Get-AzureRmStreamAnalyticsJob.md)

[새로운 AzureRmStreamAnalyticsJob](./New-AzureRmStreamAnalyticsJob.md)

[제거-AzureRmStreamAnalyticsJob](./Remove-AzureRmStreamAnalyticsJob.md)

[중지-AzureRmStreamAnalyticsJob](./Stop-AzureRmStreamAnalyticsJob.md)


