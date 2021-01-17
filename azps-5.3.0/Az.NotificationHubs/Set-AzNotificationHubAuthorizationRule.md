---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: f95b016380f640154533f69d3942b8fe12a064d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385036"
---
# Set-AzNotificationHubAuthorizationRule

## SYNOPSIS
알림 허브에 대한 권한 부여 규칙을 설정합니다.

## 구문

### InputFileParameterSet
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Set-AzNotificationHubAuthorizationRule** cmdlet은 알림 허브에 할당된 SAS(공유 액세스 서명) 권한 부여 규칙을 수정합니다.
권한 부여 규칙은 다른 사용 권한 수준에 따라 URIS로 링크를 만들어 알림 허브에 대한 액세스를 관리합니다.
사용 권한 수준은 다음 중 하나일 수 있습니다. 
- 수신
- 보내기
- 관리 클라이언트는 적절한 사용 권한 수준에 따라 이러한 UR 중 하나로 연결됩니다.
예를 들어 수신 권한이 부여된 클라이언트는 해당 권한에 대한 URI로 연결됩니다.
이 cmdlet은 알림 허브에 할당된 권한 부여 규칙을 수정하는 두 가지 방법을 제공 합니다.
하나의 경우 **SharedAccessAuthorizationRuleAttributes** 개체의 인스턴스를 만든 다음 규칙에서 소유할 속성 값으로 해당 개체를 구성할 수 있습니다.
.NET Framework를 통해 개체를 구성할 수 있습니다.
그런 다음 *SASRule* 매개 변수를 사용하여 해당 속성 값을 규칙에 복사할 수 있습니다.
또는 관련 구성 값을 포함하는 JSON(JavaScript Object Notation) 파일을 만든 다음 *InputFile* 매개 변수를 통해 해당 값을 적용할 수 있습니다.
JSON 파일은 { "Name": "ContosoAuthorizationRule",  
  "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",  
  "Rights": \[  
        "수신",  
        "보내기"  
    \]  
  } New-AzNotificationHubAuthorizationRule cmdlet과 함께 사용하는 경우 앞의 JSON 샘플은 사용자에게 허브에 수신 및 보내기 권한을 부여하기 위해 ContosoAuthorizationRule이라는 권한 부여 규칙을 수정합니다.

## 예제

### 예제 1: 알림 허브에 할당된 권한 부여 규칙 수정
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

이 명령은 ContosoExternalHub라는 알림 허브에 할당된 권한 부여 규칙을 수정합니다.
허브가 있는 네임스페이스와 허브가 할당된 리소스 그룹을 지정해야 합니다.
수정된 규칙에 대한 정보는 명령 자체에 포함되지 않습니다.
대신, 해당 정보는 입력 파일에서 찾을 수 C:\Configuration\AuthorizationRules.js.

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

### -Force
확인을 요청하지 않습니다.

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

### -InputFile
새 규칙에 대한 구성 정보를 포함하는 JSON 파일의 경로를 지정합니다.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
알림 허브가 할당된 네임스페이스를 지정합니다.
네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.

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

### -NotificationHub
이 cmdlet이 권한 부여 규칙을 할당하는 알림 허브를 지정합니다.
알림 허브는 해당 클라이언트에서 사용하는 경우와 관계없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
알림 허브가 할당된 리소스 그룹을 지정합니다. 리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.

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
수정된 권한 부여 규칙에 대한 구성 정보를 포함하는 **SharedAccessAuthorizationRuleAttributes** 개체를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 3
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

[New-AzNotificationHubAuthorizationRule](./New-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)


