---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 062d16155d4e1644e09f914a1114741e7bc5365f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336254"
---
# Get-AzNotificationHubListKey

## SYNOPSIS
알림 허브 권한 부여 규칙과 연결된 기본 및 보조 연결 문자열을 얻습니다.

## 구문

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzNotificationHubListKey** cmdlet은 알림 허브 SAS(공유 액세스 서명) 권한 부여 규칙의 기본 및 보조 연결 문자열을 반환합니다.
권한 부여 규칙은 허브에 대한 사용자 권한을 관리합니다.
각 규칙에는 기본 및 보조 연결 문자열이 포함됩니다.
이러한 연결 문자열(UR)은 다음을 수행 합니다.
- 사용자가 리소스를 보게 합니다.
- 쿼리 매개 변수를 포함하는 토큰을 포함합니다.
이러한 매개 변수 중 하나인 서명은 사용자를 인증하고 지정된 수준의 액세스를 제공하는 데 사용됩니다.

## 예제

### 예제 1: 권한 부여 규칙에 대한 기본 및 보조 연결 문자열을 얻습니다.
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

이 명령은 ContosoInternalHub 알림 허브에 할당된 규칙인 ListenRule 권한 부여 규칙에 대한 기본 및 보조 연결 문자열을 얻습니다.
명령에는 허브 네임스페이스 및 리소스 그룹이 포함되어야 합니다.

## PARAMETERS

### -AuthorizationRule
SAS(공유 액세스 서명) 인증 규칙의 이름을 지정합니다.
이러한 규칙은 사용자가 알림 허브에 대한 액세스 유형을 결정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
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
알림 허브는 해당 클라이언트에서 사용하는 플랫폼에 관계없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.

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
알림 허브가 할당된 리소스 그룹을 지정합니다.
리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys

## 참고 사항

## 관련 링크

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)


