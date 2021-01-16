---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 6f53573c6eb737d280ac24182ed84158d63d132f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494266"
---
# Register-AzAutomationScheduledRunbook

## SYNOPSIS
Runbook을 일정에 연결합니다.

## 구문

### ByRunbookName(기본값)
```
Register-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookNameAndScheduleName
```
Register-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Parameters <IDictionary>]
 [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Register-AzAutomationScheduledRunbook** cmdlet은 일정에 Azure Automation Runbook을 연결합니다.
*Runbook은 ScheduleName* 매개 변수를 사용하여 지정한 일정에 따라 시작됩니다.

## 예제

### 예제 1: 일정과 Runbook 연결
```powershell
PS C:\>Register-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

이 명령은 Runbk01이라는 Runbook을 Contoso17이라는 Azure Automation 계정의 Sched01 일정과 연결합니다.

### 예제 2

Runbook을 일정에 연결합니다. (자동Generated)

<!-- Aladdin Generated Example -->
```powershell
Register-AzAutomationScheduledRunbook -AutomationAccountName 'Contoso17' -Parameters <IDictionary> -ResourceGroupName 'ResourceGroup01' -RunbookName 'Runbk01' -ScheduleName 'Sched01'
```

## PARAMETERS

### -AutomationAccountName
이 cmdlet이 작동하는 Runbook에 대한 Automation 계정을 지정합니다.

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
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -Parameters
키/값 쌍의 해시 테이블을 지정합니다.
키는 Runbook 매개 변수 이름입니다.
값은 Runbook 매개 변수 값입니다.
Runbook이 연결된 일정에 대한 응답으로 시작되면 이러한 매개 변수가 Runbook에 전달됩니다.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
예약된 Runbook에 대한 리소스 그룹의 이름을 지정합니다.

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
이 cmdlet이 일정에 연결한 Runbook의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunOn
Hybrid Runbook Worker 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleName
이 cmdlet이 Runbook을 연결한 일정의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Automation.Model.JobSchedule

## 참고 사항

## 관련 링크

[Get-AzAutomationScheduledRunbook](./Get-AzAutomationScheduledRunbook.md)

[Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md)


