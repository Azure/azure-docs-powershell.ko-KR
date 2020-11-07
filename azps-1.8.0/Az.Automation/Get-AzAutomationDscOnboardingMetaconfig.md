---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 0302803568bac71baed28615552848f113da32df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701620"
---
# Get-AzAutomationDscOnboardingMetaconfig

## SYNOPSIS
메타 구성 .mof 파일을 만듭니다.

## 구문과

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzAutomationDscOnboardingMetaconfig** CMDLET은 DSC (원하는 상태 구성) 메타 구성 관리 개체 형식 (MOF) 파일을 만듭니다.
이 cmdlet은 사용자가 지정 하는 각 컴퓨터 이름에 대 한 .mof 파일을 만듭니다.
Cmdlet은 .mof 파일에 대 한 폴더를 만듭니다.
이 폴더에 대 한 Set-DscLocalConfigurationManager cmdlet을 실행 하 여 이러한 컴퓨터를 DSC 노드로 Azure Automation 계정으로 통합할 수 있습니다.

## 예제의

### 예제 1: 자동화 DSC에 대 한 온보드 서버
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

첫 번째 명령은 Contoso17 이라는 자동화 계정에 대 한 두 서버에 대해 DSC 메타 구성 파일을 만듭니다.
이 명령은 바탕 화면에 이러한 파일을 저장 합니다.
두 번째 명령은 **Set-DscLocalConfigurationManager** cmdlet을 사용 하 여 지정 된 컴퓨터에 meta 구성을 적용 하 여 DSC 노드로 내장 합니다.

## 변수

### -AutomationAccountName
Automation 계정의 이름을 지정 합니다.
*ComputerName* 매개 변수에서 지정 하는 컴퓨터를이 매개 변수에서 지정 하는 계정에 온보드 할 수 있습니다.

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
이 cmdlet이 .mof 파일을 생성 하는 컴퓨터의 이름 배열을 지정 합니다.
이 매개 변수를 지정 하지 않으면 cmdlet에서 현재 컴퓨터 (localhost)에 대 한 .mof 파일을 생성 합니다.

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

### -Force
확인 메시지를 표시 하지 않고 명령을 강제로 실행 하 고 동일한 이름을 가진 기존 .mof 파일을 바꿉니다.

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
이 cmdlet에서 .mof 파일을 저장 하는 폴더의 이름을 지정 합니다.

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
리소스 그룹의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹의 온보드 컴퓨터로 .mof 파일을 만듭니다.

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

### System. 문자열

### System.webserver []

## 출력

### DscOnboardingMetaconfig를 통해 서.

## 상속자

## 관련 링크
