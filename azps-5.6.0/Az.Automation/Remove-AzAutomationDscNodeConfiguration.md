---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 15e7169d0824a16832e8cf8a9ece2344474aac8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004779"
---
# Remove-AzAutomationDscNodeConfiguration

## SYNOPSIS
Automation의 DSC 노드 구성에서 메타데이터를 제거합니다.

## 구문

```
Remove-AzAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Remove-AzAutomationDscNodeConfiguration** cmdlet은 Azure Automation의 APS 원하는 상태 구성(DSC) 노드 구성에서 메타데이터를 제거합니다.
Automation은 DSC 노드 구성을 MOF(관리 개체 형식) 구성 문서로 저장합니다.

## 예제

### 예제 1

Automation의 DSC 노드 구성에서 메타데이터를 제거합니다. (자동 재생)

<!-- Aladdin Generated Example -->
```powershell
Remove-AzAutomationDscNodeConfiguration -AutomationAccountName 'AutomationAccount01' -IgnoreNodeMappings -Name 'Configuration01' -ResourceGroupName myresourcegroup
```

## 매개 변수

### -AutomationAccountName
이 cmdlet에서 메타데이터를 제거하는 DSC 노드 구성을 포함하는 Automation 계정의 이름을 지정합니다.

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

### -Force
ps_force

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreNodeMappings
이 cmdlet은 노드 매핑을 무시합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
이 cmdlet에서 메타데이터를 제거하는 DSC 노드 구성의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 리소스 그룹의 DSC 노드 구성에 대한 메타데이터를 제거합니다.

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

## 출력

### System.Void

## 참고 사항

## 관련 링크

[Get-AzAutomationDscNodeConfiguration](./Get-AzAutomationDscNodeConfiguration.md)

[Import-AzAutomationDscNodeConfiguration](./Import-AzAutomationDscNodeConfiguration.md)

[Azure Automation Cmdlet](/powershell/module/Az.Automation/)
