---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: a8d0244b9a26616e796a4e867a193da4ed3888d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697854"
---
# Get-AzAutomationDscNodeReport

## SYNOPSIS
DSC 노드에서 자동화로 전송 되는 보고서를 가져옵니다.

## 구문과

### ByAll (기본값)
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### 최신 버전
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzAutomationDscNodeReport** CMDLET은 DSC (Ap 원하는 상태 구성) 노드에서 Azure Automation으로 보낸 보고서를 가져옵니다.

## 예제의

### 예제 1: DSC 노드에 대 한 모든 보고서 가져오기
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

첫 번째 명령은 Contoso17 이라는 Automation 계정에서 Computer14 이라는 컴퓨터에 대 한 DSC 노드를 가져옵니다.
이 명령은 $Node 변수에이 개체를 저장 합니다.
두 번째 명령은 Computer14 이라는 DSC 노드에서 Contoso17 이라는 Automation 계정으로 전송 된 모든 보고서에 대 한 메타 데이터를 가져옵니다.
이 명령은 $Node 개체의 **Id** 속성을 사용 하 여 노드를 지정 합니다.

### 예제 2: 보고서 ID를 기준으로 DSC 노드에 대 한 보고서 가져오기
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

첫 번째 명령은 Contoso17 이라는 Automation 계정에서 Computer14 이라는 컴퓨터에 대 한 DSC 노드를 가져옵니다.
이 명령은 $Node 변수에이 개체를 저장 합니다.
두 번째 명령은 Computer14 이라는 DSC 노드에서 Contoso17 이라는 자동화 계정으로 보낸 지정 된 ID로 식별 되는 보고서의 메타 데이터를 가져옵니다.

### 예제 3: DSC 노드에 대 한 최신 보고서 가져오기
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

첫 번째 명령은 Contoso17 이라는 Automation 계정에서 Computer14 이라는 컴퓨터에 대 한 DSC 노드를 가져옵니다.
이 명령은 $Node 변수에이 개체를 저장 합니다.
두 번째 명령은 Computer14 이라는 DSC 노드에서 Contoso17 이라는 자동화 계정으로 전송 된 최신 보고서의 메타 데이터를 가져옵니다.

## 변수

### -AutomationAccountName
Automation 계정의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 계정에 속하는 DSC 노드에 대 한 보고서를 내보냅니다.

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
종료 시간을 지정 합니다.
이 cmdlet은이 시간 전에 자동으로 받은 보고서를 가져옵니다.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Id
이 cmdlet이 가져올 DSC 노드 보고서의 고유 ID를 지정 합니다.

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -최신 버전
이 cmdlet이 지정 된 노드에 대 한 최신 DSC 보고서를 가져옵니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeId
이 cmdlet에서 보고서를 가져올 DSC 노드의 고유 ID를 지정 합니다.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet에서 보고서를 가져올 DSC 노드가 포함 된 리소스 그룹의 이름을 지정 합니다.

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

### -StartTime
시작 시간을 지정 합니다.
이 cmdlet은이 시간 이후에 자동으로 받은 보고서를 가져옵니다.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

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

### 시스템 Null 허용 ' 1 [[CoreLib, System.webserver, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]

### System. 문자열

## 출력

### Microsoft Azure.-DscNode

## 상속자

## 관련 링크

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[Export-AzAutomationDscNodeReportContent](./Export-AzAutomationDscNodeReportContent.md)


