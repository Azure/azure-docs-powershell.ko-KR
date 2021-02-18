---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206416"
---
# New-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
권한 부여 규칙을 만들고 해당 규칙을 알림 허브 네임스페이스에 할당합니다.

## 구문

### InputFileParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명
**New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet은 SAS(공유 액세스 서명) 권한 부여 규칙을 만들고 알림 허브 네임스페이스에 할당합니다.
권한 부여 규칙은 네임스페이스 및 해당 네임스페이스에 포함된 알림 허브에 대한 사용자 권한을 관리합니다.
이 cmdlet은 새 권한 부여 규칙을 만들고 네임스페이스에 할당하는 두 가지 방법을 제공 합니다.
**SharedAccessAuthorizationRuleAttributes** 개체의 인스턴스를 만든 다음 새 규칙에서 소유하려는 속성 값으로 해당 개체를 구성할 수 있습니다.
.NET Framework를 사용하여 이 방법을 사용할 수 있습니다.
그런 다음 *SASRule* 매개 변수를 사용하여 해당 속성 값을 새 규칙에 복사할 수 있습니다.
또는 관련 구성 값을 포함하는 JSON(JavaScript Object Notation) 파일을 만든 다음 *InputFile* 매개 변수를 사용하여 해당 값을 적용할 수 있습니다.
JSON 파일은 {과 유사한 구문을 사용하는 텍스트 파일입니다.  
    "Name": "ContosoAuthorizationRule",  
    "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",  
    "Rights": \[  
        "Listen",  
        "보내기"  
    \]  
} **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet과 함께 사용하는 경우 이전 JSON 샘플은 사용자에게 네임스페이스에 대한 수신 및 보내기 권한을 부여하는 ContosoAuthorizationRule이라는 권한 부여 규칙을 만듭니다.
인증에 사용되는 *PrimaryKey는* 다음 Windows PowerShell 명령을 사용하여 임의로 생성될 수 있습니다. \[ Convert \] ::ToBase64String((1..32 |% { \[ byte/](Get-Random -Minimum 0 -Maximum 255) }))

## 예제

### 예제 1: 권한 부여 규칙을 만들고 네임스페이스에 할당
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

이 명령은 권한 부여 규칙을 만들고 해당 규칙을 네임스페이스 ContosoNamespace에 할당합니다.
이 규칙을 만들 때 네임스페이스가 할당된 적절한 네임스페이스 및 리소스 그룹을 지정해야 합니다.
그러나 규칙 자체에 대한 정보를 지정할 필요는 없습니다. 규칙 정보는 규칙이 설정되어 있는 입력 파일에서 C:\Configuration\NamespaceAuthorizationRules.js.

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

### -InputFile
새 권한 부여 규칙에 대한 구성 정보를 포함하는 JSON 파일의 경로를 지정합니다.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
권한 부여 규칙이 할당될 네임스페이스를 지정합니다.
네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.
새 규칙을 기존 네임스페이스에 할당해야 합니다.
**New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet은 새 네임스페이스를 만들 수 없습니다.

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

### -ResourceGroup
네임스페이스가 할당되는 리소스 그룹을 지정합니다.
리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.
기존 리소스 그룹을 사용해야 합니다.
이 cmdlet은 새 리소스 그룹을 만들 수 없습니다.

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

### -SASRule
새 규칙에 대한 구성 정보를 포함하는 **SharedAccessAuthorizationRuleAttributes** 개체를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
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

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## 참고 사항

## 관련 링크

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


