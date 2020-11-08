---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 5cfdf1eb7bfbb08d0658f4245d9e45804403135f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215937"
---
# New-AzNotificationHubAuthorizationRule

## SYNOPSIS
권한 부여 규칙을 만들고 알림 허브에 규칙을 할당 합니다.

## 구문과

### InputFileParameterSet
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzNotificationHubAuthorizationRule** cmdlet은 알림 허브 Sa (공유 액세스 서명) 권한 부여 규칙을 만듭니다.
인증 규칙은 알림 허브에 대 한 액세스를 관리 하는 데 사용 됩니다.
이 작업은 다양 한 사용 권한 수준에 따라 Uri로 링크를 만들어 수행 합니다.
클라이언트는 적절 한 사용 권한 수준에 따라 이러한 Uri 중 하나로 리디렉션됩니다.
예를 들어 Listen 권한이 지정 된 클라이언트는 해당 권한의 URI로 리디렉션됩니다.

## 예제의

### 예제 1: 알림 허브 권한 부여 규칙 만들기
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

이 명령은 새 권한 부여 규칙을 만들어 ContosoInternalHub 이라는 알림 허브에 할당 합니다.
이 허브는 ContosoNamespace 네임 스페이스에 있으며 ContosoNotificationsGroup 리소스 그룹에 할당 됩니다.
규칙 이름을 포함 하 여 해당 규칙에 대 한 모든 구성 정보는 C:\Configuration\ExternalAccessRule.js입력 파일에서 가져온 것을 참고 하세요.

## 변수

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

### -InputFile
이 cmdlet이 만드는 권한 부여 규칙에 대 한 입력 파일을 지정 합니다.

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
권한 부여 규칙이 할당 되는 네임 스페이스를 지정 합니다.
네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.

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
권한 부여 규칙이 할당 될 알림 허브를 지정 합니다.
알림 허브는 해당 클라이언트에서 사용 하는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.
기존 알림 허브의 이름을 지정 해야 한다는 점에 유의 하세요.
**AzNotificationHubAuthorizationRule** cmdlet은 새 알림 허브를 만들 수 없습니다.

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
알림 허브가 할당 된 리소스 그룹을 지정 합니다.

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
새 규칙에 대 한 구성 정보를 포함 하는 **Sharedaccessauthorizationruleattributes** 개체를 지정 합니다.

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Microsoft. Azure. 명령. SharedAccessAuthorizationRuleAttributes

## 상속자

## 관련 링크

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[제거-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


