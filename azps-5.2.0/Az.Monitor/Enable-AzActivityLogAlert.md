---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 6e3414efd21b1dd333f91e24333cda05ea650600
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343430"
---
# Enable-AzActivityLogAlert

## SYNOPSIS
활동 로그 경고를 설정하고 해당 태그를 설정합니다.

## 구문

### EnableByNameAndResourceGroup
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EnableByInputObject
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EnableByResourceId
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**Enable-AzActivityLogAlert** cmdlet을 사용하면 활동 로그 경고를 사용하도록 설정하고 해당 태그를 설정할 수 있습니다.
이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 패치하기 전에 사용자로부터 확인을 요청할 수 있습니다.

## 예제

### 예제 1: 활동 로그 경고 사용
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

이 명령은 리소스 그룹 Default-ActivityLogsAlerts에서 alert1이라는 활동 로그 경고를 사용할 수 있습니다.

### 예제 2: PSActivityLogAlertResource 개체를 입력으로 사용하여 활동 로그 경고 사용
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

이 명령은 alert1이라는 활동 로그 경고를 사용할 수 있습니다. 이를 위해 PSActivityLogAlertResource 개체를 입력 인수로 사용합니다.

### 예제 3: ResourceId 매개 변수를 사용하여 ActivityLogAlert 사용
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

이 명령은 파이프의 ResourceId 매개 변수를 사용하여 ActivityLogAlert를 사용할 수 있습니다.

## PARAMETERS

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

### -InputObject
호출의 InputObject 태그 속성을 설정하여 필요한 이름, 리소스 그룹 이름 및 선택적 태그 속성을 추출합니다.

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
활동 로그 경고의 이름입니다.

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
경고 리소스가 존재할 리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
호출의 ResourceId 태그 속성을 설정하여 필요한 이름, 리소스 그룹 이름 속성을 추출합니다.

```yaml
Type: System.String
Parameter Sets: EnableByResourceId
Aliases:

Required: True
Position: Named
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource

## 출력

### Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource

## 참고 사항

## 관련 링크

[Set-AzActivityLogAlert](./Set-AzActivityLogAlert.md)

[Get-AzActivityLogAlert](./Get-AzActivityLogAlert.md)

[Remove-AzActivityLogAlert](./Remove-AzActivityLogAlert.md)

[New-AzActionGroup](./New-AzActionGroup.md)

[New-AzActivityLogAlertCondition](./New-AzActivityLogAlertCondition.md)

[Disable-AzActivityLogAlert](./Disable-AzActivityLogAlert.md)
