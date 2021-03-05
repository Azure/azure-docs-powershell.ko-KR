---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: e520fec3d0299ca2b5f74bb2a8a8b7de437d7a2a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008155"
---
# Get-AzAutomationDscOnboardingMetaconfig

## SYNOPSIS
메타 구성 .mof 파일을 만듭니다.

## 구문

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Get-AzAutomationDscOnboardingMetaconfig** cmdlet은 APS 원하는 상태 구성(DSC) 메타 구성 관리 개체 형식(MOF) 파일을 만듭니다.
이 cmdlet은 지정한 각 컴퓨터 이름에 대해 .mof 파일을 만듭니다.
cmdlet은 .mof 파일에 대한 폴더를 만듭니다.
이 폴더의 Set-DscLocalConfigurationManager cmdlet을 실행하여 이러한 컴퓨터를 DSC 노드로 Azure Automation 계정에 온보드할 수 있습니다.

## 예제

### 예제 1: Automation DSC에 서버 온보드
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

첫 번째 명령은 Contoso17이라는 Automation 계정의 두 서버에 대해 DSC 메타 구성 파일을 만듭니다.
명령은 데스크톱에 이러한 파일을 저장합니다.
두 번째 명령은 **Set-DscLocalConfigurationManager** cmdlet을 사용하여 지정된 컴퓨터에 메타 구성을 적용하여 DSC 노드로 온보드합니다.

## 매개 변수

### -AutomationAccountName
Automation 계정의 이름을 지정합니다.
*ComputerName* 매개 변수가 이 매개 변수가 지정하는 계정에 지정하는 컴퓨터를 온보드할 수 있습니다.

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

### -ComputerName
이 cmdlet에서 .mof 파일을 생성하는 컴퓨터의 이름 배열을 지정합니다.
이 매개 변수를 지정하지 않으면 cmdlet은 현재 컴퓨터(localhost)에 대한 .mof 파일을 생성합니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -Force
확인을 묻는 메시지를 표시하지 않고 명령을 강제로 실행하고 이름이 동일한 기존 .mof 파일을 대체합니다.

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

### -OutputFolder
이 cmdlet에서 .mof 파일을 저장하는 폴더의 이름을 지정합니다.

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

### -ResourceGroupName
리소스 그룹의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 리소스 그룹의 컴퓨터에 온보드할 .mof 파일을 만듭니다.

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
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

### System.String[]

## 출력

### Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig

## 참고 사항

## 관련 링크
