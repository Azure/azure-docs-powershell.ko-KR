---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: bb88bc38f6102f18b4d45b3b80902886975e2628
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987051"
---
# Get-AzAutomationDscNodeReport

## SYNOPSIS
DSC 노드에서 Automation으로 전송된 보고서를 제공합니다.

## 구문

### ByAll(기본값)
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByLatest
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzAutomationDscNodeReport** cmdlet은 APS 원하는 상태 구성(DSC) 노드에서 Azure Automation으로 전송된 보고서를 얻습니다.

## 예제

### 예제 1: DSC 노드에 대한 모든 보고서 사용
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

첫 번째 명령은 Contoso17이라는 Automation 계정에서 Computer14라는 컴퓨터에 대한 DSC 노드를 얻습니다.
명령은 이 개체를 $Node 저장합니다.
두 번째 명령은 Computer14라는 DSC 노드에서 Contoso17이라는 Automation 계정으로 전송된 모든 보고서의 메타데이터를 얻습니다.
명령은 개체의 **ID** 속성을 사용하여 노드를 $Node 지정합니다.

### 예제 2: 보고서 ID로 DSC 노드에 대한 보고서 얻습니다.
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

첫 번째 명령은 Contoso17이라는 Automation 계정에서 Computer14라는 컴퓨터에 대한 DSC 노드를 얻습니다.
명령은 이 개체를 $Node 저장합니다.
두 번째 명령은 Computer14라는 DSC 노드에서 Contoso17이라는 Automation 계정으로 전송된 지정된 ID로 식별된 보고서의 메타데이터를 얻습니다.

### 예제 3: DSC 노드에 대한 최신 보고서 다운로드
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

첫 번째 명령은 Contoso17이라는 Automation 계정에서 Computer14라는 컴퓨터에 대한 DSC 노드를 얻습니다.
명령은 이 개체를 $Node 저장합니다.
두 번째 명령은 Computer14라는 DSC 노드에서 Contoso17이라는 Automation 계정으로 전송된 최신 보고서의 메타데이터를 얻습니다.

## 매개 변수

### -AutomationAccountName
Automation 계정의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 계정에 속하는 DSC 노드에 대한 보고서를 내보낼 수 있습니다.

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
azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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
종료 시간을 지정합니다.
이 cmdlet은 자동화가 이 시간 전에 수신한 보고서를 수신합니다.

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
이 cmdlet에서 얻을 DSC 노드 보고서의 고유 ID를 지정합니다.

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

### -Latest
이 cmdlet은 지정된 노드에만 대한 최신 DSC 보고서를 을 를 나타냅니다.

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
이 cmdlet에서 보고서를 얻을 수 있는 DSC 노드의 고유 ID를 지정합니다.

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
이 cmdlet에서 보고서를 받을 DSC 노드를 포함하는 리소스 그룹의 이름을 지정합니다.

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
시작 시간을 지정합니다.
이 cmdlet은 자동화가 이 시간 이후에 수신한 보고서를 수신합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.Guid

### System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String

## 출력

### Microsoft.Azure.Commands.Automation.Model.DscNode

## 참고 사항

## 관련 링크

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[Export-AzAutomationDscNodeReportContent](./Export-AzAutomationDscNodeReportContent.md)


