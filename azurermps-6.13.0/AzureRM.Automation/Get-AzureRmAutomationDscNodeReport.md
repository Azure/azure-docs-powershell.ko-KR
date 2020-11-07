---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: 747ffdb9df955609a38718016af50bb5434c0224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703493"
---
# Get-AzureRmAutomationDscNodeReport

## SYNOPSIS
DSC 노드에서 자동화로 전송 되는 보고서를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByAll (기본값)
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### 최신 버전
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmAutomationDscNodeReport** CMDLET은 DSC (Ap 원하는 상태 구성) 노드에서 Azure Automation으로 보낸 보고서를 가져옵니다.

## 예제의

### 예제 1: DSC 노드에 대 한 모든 보고서 가져오기
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

첫 번째 명령은 Contoso17 이라는 Automation 계정에서 Computer14 이라는 컴퓨터에 대 한 DSC 노드를 가져옵니다.
이 명령은 $Node 변수에이 개체를 저장 합니다.
두 번째 명령은 Computer14 이라는 DSC 노드에서 Contoso17 이라는 Automation 계정으로 전송 된 모든 보고서에 대 한 메타 데이터를 가져옵니다.
이 명령은 $Node 개체의 **Id** 속성을 사용 하 여 노드를 지정 합니다.

### 예제 2: 보고서 ID를 기준으로 DSC 노드에 대 한 보고서 가져오기
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

첫 번째 명령은 Contoso17 이라는 Automation 계정에서 Computer14 이라는 컴퓨터에 대 한 DSC 노드를 가져옵니다.
이 명령은 $Node 변수에이 개체를 저장 합니다.
두 번째 명령은 Computer14 이라는 DSC 노드에서 Contoso17 이라는 자동화 계정으로 보낸 지정 된 ID로 식별 되는 보고서의 메타 데이터를 가져옵니다.

### 예제 3: DSC 노드에 대 한 최신 보고서 가져오기
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### 시스템 Null 허용 ' 1 [[b77a5c561934e089] [[System.webserver, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]

### System. 문자열

## 출력

### Microsoft Azure.-DscNode

## 상속자

## 관련 링크

[Get-AzureRmAutomationDscNode](./Get-AzureRmAutomationDscNode.md)

[Export-AzureRmAutomationDscNodeReportContent](./Export-AzureRmAutomationDscNodeReportContent.md)


