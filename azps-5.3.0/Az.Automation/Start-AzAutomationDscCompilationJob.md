---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 34f09ca41326b2f6686a41cdeba0910317bc7a2c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494208"
---
# Start-AzAutomationDscCompilationJob

## SYNOPSIS
Automation에서 DSC 구성을 컴파일합니다.

## 구문

```
Start-AzAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**Start-AzAutomationDscCompilationJob** cmdlet은 Azure Automation에서 APS DSC(Desired State Configuration) 구성을 컴파일합니다.

## 예제

### 예제 1: Automation에서 Azure DSC 구성 컴파일
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

첫 번째 명령은 매개 변수의 사전을 만들고 매개 변수에 $Params 저장합니다.
두 번째 명령은 Config01이라는 DSC 구성을 컴파일합니다.
이 명령은 DSC 구성 매개 변수에 대한 $Params 값을 포함합니다.

### 예제 2: 새 노드 구성 빌드 버전을 사용하여 Automation에서 Azure DSC 구성을 컴파일합니다.
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

첫 번째 예제와 마찬가지로 첫 번째 명령은 매개 변수 사전을 만들고 매개 변수의 $Params 저장합니다.
두 번째 명령은 Config01이라는 DSC 구성을 컴파일합니다.
이 명령은 DSC 구성 매개 변수에 대한 $Params 값을 포함합니다.
Config01[<2 /> 이름으로 새 노드 구성을 만들어서 이전의 기존 노드 구성을>. <NodeName> 버전 번호는 이미 있는 기존 버전 번호에 따라 증분됩니다.

## PARAMETERS

### -AutomationAccountName
이 cmdlet이 컴파일하는 DSC 구성을 포함하는 Automation 계정의 이름을 지정합니다.

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

### -ConfigurationData
DSC 구성에 대한 구성 데이터의 사전을 지정합니다.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConfigurationName
이 cmdlet이 컴파일하는 DSC 구성의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
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

### -IncrementNodeConfigurationBuild
새 노드 구성 빌드 버전을 만듭니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parameters
이 cmdlet이 DSC 구성을 컴파일하는 데 사용하는 매개 변수 사전을 지정합니다.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet이 구성을 컴파일하는 리소스 그룹의 이름을 지정합니다.

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

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### Microsoft.Azure.Commands.Automation.Model.CompilationJob

## 참고 사항

## 관련 링크

[Get-AzAutomationDscCompilationJob](./Get-AzAutomationDscCompilationJob.md)

[Get-AzAutomationDscCompilationJobOutput](./Get-AzAutomationDscCompilationJobOutput.md)


