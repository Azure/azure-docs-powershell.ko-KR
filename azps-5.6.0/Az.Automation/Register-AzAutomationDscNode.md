---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: ceae5a9e7dec9913d90aae836784c6bfe66b680f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010000"
---
# Register-AzAutomationDscNode

## SYNOPSIS
Automation 계정에 대한 DSC 노드로 Windows OS를 실행하는 Azure 가상 머신을 등록합니다.

## 구문

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Register-AzAutomationDscNode** cmdlet은 Azure Automation 계정에 APS 원하는 상태 구성(DSC) 노드로 Azure 가상 머신을 등록합니다. 이 cmdlet은 계정에 대한 Automation DSC 노드로 Windows OS를 실행하는 VM만 등록합니다.

다른 구독에서 자동화 계정에 노드를 등록해야 하는 경우 cmdlet이 ARM 템플릿을 사용해야 합니다. 자세한 내용은 Azure [Automation](https://docs.microsoft.com/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) 설명서를 참조하세요.

## 예제

### 예제 1: Azure DSC 노드로 Azure 가상 머신 등록
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

이 명령은 Contoso17이라는 Automation 계정에 VirtualMachine01이라는 Azure 가상 머신을 DSC 노드로 등록합니다.

## 매개 변수

### -ActionAfterReboot
가상 머신이 다시 시작한 후 수행한 작업을 지정합니다.
유효한 값은: 
- ContinueConfiguration 
- StopConfiguration

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AllowModuleOverwrite
Azure Automation DSC 끌어오기 서버에서 이 DSC 노드가 다운로드하는 새 구성이 대상 노드의 기존 모듈을 대체하는지 여부를 지정합니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutomationAccountName
이 cmdlet이 가상 머신을 등록하는 Automation 계정의 이름을 지정합니다.

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

### -AzureVMLocation
Azure VM 위치입니다.

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

### -AzureVMName
Azure Automation DSC에 관리를 등록할 Azure 가상 머신의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMResourceGroup
Azure VM 리소스 그룹 이름입니다.

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

### -ConfigurationMode
DSC 구성 모드를 지정합니다.
유효한 값은: 
- ApplyAndMonitor 
- ApplyAndAutocorrect 
- ApplyOnly

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationModeFrequencyMins
DSC의 백그라운드 애플리케이션이 대상 노드에서 현재 구성을 구현하려고 시도하는 빈도를 분으로 지정합니다.

```yaml
Type: System.Int32
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

### -NodeConfigurationName
이 cmdlet이 Azure Automation DSC에서 끌어오도록 가상 머신을 구성하는 노드 구성의 이름을 지정합니다.

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

### -RebootNodeIfNeeded
필요한 경우 가상 머신을 다시 시작할지 여부를 지정합니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RefreshFrequencyMins
로컬 Configuration Manager가 Azure Automation DSC 끌어오기 서버에 문의하여 최신 노드 구성을 다운로드하는 빈도를 몇 분 만에 지정합니다.

```yaml
Type: System.Int32
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
이 cmdlet이 가상 머신을 등록하는 Automation 계정은 이 매개 변수가 지정하는 리소스 그룹에 속합니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

### System.Int32

### System.Boolean

## 출력

### System.Void

## 참고 사항

## 관련 링크

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[Set-AzAutomationDscNode](./Set-AzAutomationDscNode.md)

[Unregister-AzAutomationDscNode](./Unregister-AzAutomationDscNode.md)


