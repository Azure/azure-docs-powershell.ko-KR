---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 630f32bc9dd4542ad022ed7b65ec85f6456367b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871426"
---
# Get-AzStreamAnalyticsJob

## SYNOPSIS
Stream Analytics 작업 정보를 가져옵니다.

## 구문과

### ByResourceGroup
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySubscription
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzStreamAnalyticsJob** Cmdlet은 Azure 구독 또는 지정 된 리소스 그룹에 정의 된 모든 스트림 분석 작업을 나열 하거나 리소스 그룹 내의 특정 작업에 대 한 작업 정보를 가져옵니다.

## 예제의

### 예제 1: 구독의 모든 작업에 대 한 정보 가져오기
```
PS C:\>Get-AzStreamAnalyticsJob
```

이 명령은 Azure 구독에서 모든 Stream Analytics 작업에 대 한 정보를 반환 합니다.

### 예제 2: 리소스 그룹의 모든 작업에 대 한 정보 가져오기
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

이 명령은 리소스 그룹 StreamAnalytics의 모든 Stream Analytics 작업에 대 한 정보를 반환 합니다 (기본값-서쪽-US).

### 예제 3: 리소스 그룹의 특정 작업에 대 한 정보 가져오기
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

이 명령은 리소스 그룹 StreamAnalytics의 Stream Analytics 작업 StreamingJob에 대 한 정보를 반환 합니다-기본값-미국-US.

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

### -이름
검색할 Azure Stream Analytics 작업의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NoExpand
Cmdlet이 Azure Stream Analytics 작업을 검색 하지만 입력, 출력 및 변환에 대 한 정보를 반환 하지 않음을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### System.webserver 매개 변수

## 출력

### Microsoft. Azure. PSJob.

## 상속자

## 관련 링크

[새로운 AzStreamAnalyticsJob](./New-AzStreamAnalyticsJob.md)

[제거-AzStreamAnalyticsJob](./Remove-AzStreamAnalyticsJob.md)

[시작-AzStreamAnalyticsJob](./Start-AzStreamAnalyticsJob.md)

[중지-AzStreamAnalyticsJob](./Stop-AzStreamAnalyticsJob.md)


