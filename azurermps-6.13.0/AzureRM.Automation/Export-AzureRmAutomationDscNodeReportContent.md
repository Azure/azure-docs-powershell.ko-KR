---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
ms.openlocfilehash: 52ed2c5925758a4d40fdf39dcdadf73eb2fc53b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524668"
---
# Export-AzureRmAutomationDscNodeReportContent

## SYNOPSIS
DSC 노드에서 전송 되는 DSC 보고서의 원시 콘텐츠를 자동화로 내보냅니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Export-AzureRmAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**Export-AzureRmAutomationDscNodeReportContent** CMDLET은 DSC (원하는 상태 구성) 보고서의 원시 콘텐츠를 내보냅니다.
DSC 노드에서는 DSC 보고서를 Azure 자동화로 보냅니다.

## 예제의

### 예제 1: DSC 노드에서 보고서 내보내기
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzureRmAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

이 명령 집합은 Computer14 이라는 DSC 노드에서 최신 보고서를 데스크톱으로 내보냅니다.

## 변수

### -AutomationAccountName
Automation 계정의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 자동화 계정에 속하는 DSC 노드에 대 한 보고서 콘텐츠를 내보냅니다.

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

### -Force
이 cmdlet이 기존 로컬 파일을 동일한 이름을 가진 새 파일로 대체 함을 나타냅니다.

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

### -NodeId
이 cmdlet이 보고서 콘텐츠를 내보내는 DSC 노드의 고유 ID를 지정 합니다.

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

### -OutputFolder
이 cmdlet이 보고서 콘텐츠를 내보내는 출력 폴더를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReportId
이 cmdlet이 내보내는 DSC 노드 보고서의 고유 ID를 지정 합니다.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름을 지정 합니다.
이 cmdlet은이 cmdlet에서 지정 하는 리소스 그룹에 속하는 DSC 노드에 대 한 보고서의 콘텐츠를 내보냅니다.

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

### 시스템 Guid

### System. 문자열

## 출력

### DirectoryInfo

## 상속자

## 관련 링크

[Export-AzureRmAutomationDscNodeReportContent](./Export-AzureRmAutomationDscNodeReportContent.md)

[Get-AzureRmAutomationDscNode](./Get-AzureRmAutomationDscNode.md)

[Get-AzureRmAutomationDscNodeReport](./Get-AzureRmAutomationDscNodeReport.md)


