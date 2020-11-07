---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: ae638c693366568458a4194d1625d19eaac6af93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697842"
---
# Get-AzAutomationJob

## SYNOPSIS
자동화 runbook 작업을 가져옵니다.

## 구문과

### ByAll (기본값)
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByJobId
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzAutomationJob** Cmdlet은 Azure Automation에서 runbook 작업을 가져옵니다.

## 예제의

### 예제 1: 특정 runbook 작업 가져오기
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

이 명령은 지정 된 GUID가 있는 작업을 가져옵니다.

### 예제 2: runbook에 대 한 모든 작업 가져오기
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

이 명령은 Runbook02 이라는 runbook과 연결 된 모든 작업을 가져옵니다.

### 예제 3: 실행 중인 모든 작업 가져오기
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

이 명령은 Contoso17 이라는 자동화 계정에서 실행 중인 모든 작업을 가져옵니다.

## 변수

### -AutomationAccountName
이 cmdlet이 작업을 가져오는 Automation 계정의 이름을 지정 합니다.

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

### -EndTime
작업의 종료 시간을 **DateTimeOffset** 개체로 지정 합니다.
유효한 **DateTimeOffset** 으로 변환할 수 있는 문자열을 지정할 수 있습니다.
이 cmdlet은이 매개 변수에서 지정 하는 값 또는 그 이전에 종료 시간이 있는 작업을 가져옵니다.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
이 cmdlet이 가져오는 작업의 ID를 지정 합니다.

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet이 작업을 가져오는 리소스 그룹의 이름을 지정 합니다.

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

### -RunbookName
이 cmdlet이 작업을 가져오는 runbook의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
작업의 시작 시간을 **DateTimeOffset** 개체로 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 값의 시작 시간 또는 그 이후의 작업을 가져옵니다.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -상태
작업의 상태를 지정 합니다.
이 cmdlet은이 매개 변수와 일치 하는 상태의 상태가 있는 작업을 가져옵니다.
유효한 값은 다음과 같습니다. 
- 인증과
- 완료
- 못함
- 시킵니다
- 계속
- 실행
- 시작
- 멈추었습니다
- 시작점
- 된
- 시키면

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 시스템 Guid

### System. 문자열

## 출력

### Microsoft. Azure. 작업

## 상속자

## 관련 링크

[Get-AzAutomationJobOutput](./Get-AzAutomationJobOutput.md)

[이력서-AzAutomationJob](./Resume-AzAutomationJob.md)

[중지-AzAutomationJob](./Stop-AzAutomationJob.md)

[일시 중단-AzAutomationJob](./Suspend-AzAutomationJob.md)


