---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: b139ed5b67bbc36bad45ab2528ed74299d40c1b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969712"
---
# Get-AzAutomationDscNodeConfiguration

## SYNOPSIS
Automation에서 DSC 노드 구성에 대한 메타데이터를 얻습니다.

## 구문

### ByAll(기본값)
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByNodeConfigurationName
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConfigurationName
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzAutomationDscNodeConfiguration** cmdlet은 Azure Automation의 APS 원하는 상태 구성(DSC) 노드 구성에 대한 메타데이터를 얻습니다.
Automation은 DSC 노드 구성을 MOF(관리 개체 형식) 구성 문서로 저장합니다.

## 예제

### 예제 1: 모든 DSC 노드 구성을 얻습니다.
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

이 명령은 Contoso17이라는 Automation 계정의 모든 DSC 노드 구성에 대한 메타데이터를 얻습니다.

### 예제 2: DSC 구성에 대한 모든 DSC 노드 구성을 얻습니다.
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

이 명령은 ContosoConfiguration이라는 DSC 구성이 생성된 Contoso17이라는 Automation 계정의 모든 DSC 노드 구성에 대한 메타데이터를 얻습니다.

### 예제 3: 이름에 따라 DSC 노드 구성을 얻습니다.
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

이 명령은 Contoso17이라는 Automation 계정에서 ContosoConfiguration.webserver라는 이름으로 DSC 노드 구성에 대한 메타데이터를 얻습니다.

## 매개 변수

### -AutomationAccountName
이 cmdlet에서 메타데이터를 얻을 수 있는 DSC 노드 구성을 포함하는 Automation 계정의 이름을 지정합니다.

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

### -ConfigurationName
이 cmdlet에서 노드 구성 메타데이터를 얻을 DSC 구성의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases:

Required: True
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

### -Name
이 cmdlet에서 메타데이터를 얻을 DSC 노드 구성의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 리소스 그룹의 DSC 노드 구성에 대한 메타데이터를 얻습니다.

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

### -RollupStatus
이 cmdlet이 얻을 DSC 노드 구성의 롤업 상태를 지정합니다.
유효한 값은: 
- 잘못된 
- 좋음

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Automation.Model.CompilationJob

## 참고 사항

## 관련 링크

[Import-AzAutomationDscNodeConfiguration](./Import-AzAutomationDscNodeConfiguration.md)


