---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 70d322b46f8aa9dc90696cbd813e576cc9dd9fbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326605"
---
# Start-AzAutomationRunbook

## SYNOPSIS
Runbook 작업을 시작합니다.

## 구문

### ByAsynchronousReturnJob(기본값)
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### BySynchronousReturnJobOutput
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Start-AzAutomationRunbook** cmdlet은 Azure Automation Runbook 작업을 시작합니다.
Runbook의 ID 또는 이름을 지정합니다.

## 예제

### 예제 1: Runbook 작업 시작
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

이 명령은 Contoso17이라는 Azure Automation 계정에서 Runbk01이라는 Runbook에 대한 Runbook 작업을 시작합니다.

### 예제 2: 매개 변수를 사용하여 Python 2 Runbook 작업 시작
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

이 명령은 첫 번째 위치 매개 변수로 "ValueForPosition1"과 두 번째 위치 매개 변수로 "ValueForPosition2"를 사용하여 Contoso17이라는 Azure Automation 계정에서 RunbkPy01이라는 Python 2 Runbook에 대한 Runbook 작업을 시작합니다.

### 예제 3: Runbook 작업을 시작하고 결과를 기다릴 수 있습니다.
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

이 명령은 Contoso17이라는 Azure Automation 계정에서 Runbk01이라는 Runbook에 대한 Runbook 작업을 시작합니다.
이 명령은 Wait 매개 _변수를 지정합니다._
따라서 작업이 완료된 후 결과를 반환합니다.
cmdlet은 결과를 위해 최대 1000초 동안 대기합니다.

## PARAMETERS

### -AutomationAccountName
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

### -MaxWaitSeconds
이 cmdlet이 작업을 중단하기 전에 작업이 완료될 때까지 대기하는 시간(초)을 지정합니다.
기본값은 10800 또는 3시간입니다.

```yaml
Type: System.Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parameters
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: JobParameters

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
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

### -RunOn
Runbook을 실행할 Hybrid Worker 그룹을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Wait
이 cmdlet은 작업이 완료, 일시 중단 또는 실패할 때까지 기다렸다가 Azure PowerShell에 제어를 반환합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Automation.Model.Job

### System.Management.Automation.PSObject

## 참고 사항

## 관련 링크

[Export-AzAutomationRunbook](./Export-AzAutomationRunbook.md)

[Get-AzAutomationRunbook](./Get-AzAutomationRunbook.md)

[Import-AzAutomationRunbook](./Import-AzAutomationRunbook.md)

[New-AzAutomationRunbook](./New-AzAutomationRunbook.md)

[New-AzAutomationRunbook](./New-AzAutomationRunbook.md)

[Publish-AzAutomationRunbook](./Publish-AzAutomationRunbook.md)

[Remove-AzAutomationRunbook](./Remove-AzAutomationRunbook.md)

[Set-AzAutomationRunbook](./Set-AzAutomationRunbook.md)
