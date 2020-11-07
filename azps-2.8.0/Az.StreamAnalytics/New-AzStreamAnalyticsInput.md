---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 60bc6754fb63d118e2b74e60ab503600a128ba3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874279"
---
# New-AzStreamAnalyticsInput

## SYNOPSIS
작업 입력을 만들거나 업데이트 합니다.

## 구문과

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzStreamAnalyticsInput** Cmdlet은 Stream Analytics 작업 내에 입력을 만들거나 기존 입력을 업데이트 합니다.
입력 이름은 JSON 파일 또는 명령줄에서 지정할 수 있습니다.
둘 다 지정 된 경우 명령줄의 name 명령은 파일의 이름과 일치 해야 합니다.
이미 존재 하 고 *Force* 매개 변수를 지정 하지 않은 입력을 지정 하는 경우 cmdlet은 기존 입력을 바꿀지 여부를 확인 합니다.
*Force* 매개 변수를 지정 하 고 기존 입력 이름을 지정 하면 입력이 확인 없이 바뀝니다.

## 예제의

### 예제 1: 파일의 정의를 사용 하 여 작업 입력 만들기
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

이 명령은 파일 Input.js에 대 한 입력을 만듭니다.
입력 정의 파일에 지정 된 이름을 사용 하는 기존 입력이 이미 정의 되어 있는 경우 cmdlet은이를 바꿀 것인지 여부를 확인 합니다.

### 예제 2: 작업 입력 만들기
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

이 명령은 EntryStream 이라는 작업에 새 입력을 만듭니다.
이 이름을 사용 하는 기존 입력이 이미 정의 되어 있는 경우 cmdlet은이를 바꿀 것인지 여부를 묻는 메시지를 표시 합니다.

### 예제 3: 작업 입력을 파일의 정의로 바꾸기
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

이 명령은 확인 하지 않고 파일의 정의를 사용 하 여 EntryStream 이라는 기존 입력 원본의 정의를 바꿉니다.

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

### -파일
만들 Azure Stream Analytics 입력의 JSON 표현을 포함 하는 JSON 파일의 경로를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
Azure Stream Analytics 입력을 만들 Azure Stream Analytics 작업의 이름을 지정 합니다.

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

### -이름
만들 Azure Stream Analytics 입력의 이름을 지정 합니다.

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

### -ResourceGroupName
Azure 스트리밍 입력을 만들 리소스 그룹의 이름을 지정 합니다.

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Microsoft. StreamAnalytics. PSInput

## 상속자

## 관련 링크

[Get-AzStreamAnalyticsInput](./Get-AzStreamAnalyticsInput.md)

[제거-AzStreamAnalyticsInput](./Remove-AzStreamAnalyticsInput.md)

[테스트-AzStreamAnalyticsInput](./Test-AzStreamAnalyticsInput.md)


