---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateRun.md
ms.openlocfilehash: d49d99f8edd3ffe0c25886447eac0bbd15837fc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703487"
---
# Get-AzureRmAutomationSoftwareUpdateRun

## SYNOPSIS
Azure automation 소프트웨어 업데이트 실행 목록을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByAll (기본값)
```
Get-AzureRmAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>]
 [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzureRmAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySucName
```
Get-AzureRmAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### BySuc
```
Get-AzureRmAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
Get-AzureRmAutomationSoftwareUpdateRun cmdlet은 소프트웨어 업데이트 실행 목록을 반환 합니다. 소프트웨어 업데이트 구성에는 연결 된 일정이 있으므로 여러 번 트리거될 수 있습니다. 일정을 트리거할 때마다 업데이트 실행이 생성 됩니다. 업데이트 실행은 모든 컴퓨터 실행의 결과를 집계 한 것입니다. SoftwareUpdateConfigurationName 매개 변수를 전달 하 여 특정 소프트웨어 업데이트 구성에 대 한 실행을 가져올 수 있습니다. 특정 실행을 얻으려면 name 매개 변수를 전달 해야 합니다. 특정 상태를 사용 하 여 실행을 나열 하거나, 특정 작업을 대상으로 실행 하거나, 적절 한 매개 변수를 전달 하 여 특정 시간 후에 시작 되는 실행을 나열할 수도 있습니다.

## 예제의

### 예제 1
이 예제에서는 특정 소프트웨어 업데이트 구성에 의해 트리거되는 모든 업데이트 실행을 나열 합니다.

```powershell
PS C:\> Get-AzureRmAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
                                               -AutomationAccountName "myaccount" `
                                               -SoftwareUpdateConfigurationName "MyUpdateConfiguration"

RunId                           : ec9ce57f-da18-44be-b33b-651a0f93cb52
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 11:37:42 PM +00:00
EndTime                         : 5/22/2018 11:38:31 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ec9ce57f-da18-44be-b33b-651a0f93cb52
CreationTime                    : 5/22/2018 11:37:42 PM +00:00
LastModifiedTime                : 5/22/2018 11:38:54 PM +00:00
Description                     :

RunId                           : ac9396c7-a837-43d4-be97-fbfe46c80baa
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 10:00:47 PM +00:00
EndTime                         : 5/22/2018 10:02:20 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ac9396c7-a837-43d4-be97-fbfe46c80baa
CreationTime                    : 5/22/2018 10:00:47 PM +00:00
LastModifiedTime                : 5/22/2018 10:02:58 PM +00:00
```

## 변수

### -AutomationAccountName
Automation 계정 이름입니다.

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

### -Id
소프트웨어 업데이트 구성 실행의 Id입니다.

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -비 기능
실행의 운영 체제입니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

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

### -SoftwareUpdateConfiguration
소프트웨어 업데이트 구성이 실행을 트리거 했습니다.

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SoftwareUpdateConfigurationName
실행을 트리거한 소프트웨어 업데이트 구성의 이름입니다.

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartTime
실행의 최소 시작 시간입니다.

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByAll, BySucName, BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -상태
실행 상태입니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 시스템 Guid

### System. 문자열

### UpdateManagement. SoftwareUpdateConfiguration에 대 한 자동.

### 시스템 Null 허용 ' 1 [[UpdateManagement]. OperatingSystemType, Microsoft azure. e. t e 5.1.1.0, Version =, Culture = 중립, PublicKeyToken = null]]

### 시스템 Null 허용 ' 1 [[UpdateManagement]. SoftwareUpdateRunStatus, Microsoft azure. e. t e 5.1.1.0, Version =, Culture = 중립, PublicKeyToken = null]]

### 시스템 DateTimeOffset

## 출력

### UpdateManagement. SoftwareUpdateRun에 대 한 자동.

## 상속자

## 관련 링크
