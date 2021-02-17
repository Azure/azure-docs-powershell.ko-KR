---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: 1194a730293d6f0f7b4aca58f508f808a2c6193e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182916"
---
# Start-AzStreamAnalyticsJob

## SYNOPSIS
Stream Analytics 작업을 시작합니다.

## 구문

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Start-AzStreamAnalyticsJob** cmdlet은 Azure에서 Stream Analytics 작업을 비동기적으로 배포하고 시작합니다.

## 예제

### 예제 1: Stream Analytics 작업 시작
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

이 명령은 StreamingJob 작업을 시작하고 출력 이벤트 스트림이 타임스탬프 2014-07-03T01:00Z에서 시작된다고 지정합니다.

## PARAMETERS

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

### -Name
시작할 Azure Stream Analytics 작업의 이름을 지정합니다.

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
작업의 시작 모드를 지정합니다.
유효한 값은 
- JobStartTime - 이 값은 작업이 시작되면 출력 이벤트 스트림의 시작 지점이 시작해야 한다고 나타냅니다.
- CustomTime - 이 값은 *OutputStartTime* 매개 변수에 지정된 사용자 지정 시간에서 출력 이벤트 스트림의 시작 지점이 시작될 것을 나타냅니다. 
 - LastOutputEventTime - 이 값은 출력 이벤트 스트림의 시작 지점이 마지막 이벤트 출력 시간에서 시작해야 한다고 나타냅니다.
속성이 없습니다. 기본값은 JobStartTime입니다.

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
출력 시작 시간을 지정합니다.
이 값은 출력 이벤트 스트림의 시작점을 나타내는 ISO-8601 형식의 타임스탬프 또는 $Null 시작될 때마다 출력 이벤트 스트림이 시작된다고 나타내는 타임스탬프입니다.
*OutputStartMode가 CustomTime으로* 설정된 경우 이 속성에 값이 있어야 합니다.

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
Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정합니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

### System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## 출력

### System.Boolean

## 참고 사항

## 관련 링크

[Get-AzStreamAnalyticsJob](./Get-AzStreamAnalyticsJob.md)

[New-AzStreamAnalyticsJob](./New-AzStreamAnalyticsJob.md)

[Remove-AzStreamAnalyticsJob](./Remove-AzStreamAnalyticsJob.md)

[Stop-AzStreamAnalyticsJob](./Stop-AzStreamAnalyticsJob.md)


