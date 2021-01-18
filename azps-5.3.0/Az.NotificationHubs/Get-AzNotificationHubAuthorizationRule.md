---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496447"
---
# Get-AzNotificationHubAuthorizationRule

## SYNOPSIS
알림 허브와 연결된 권한 부여 규칙에 대한 정보를 얻습니다.

## 구문

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzNotificationHubAuthorizationRule** cmdlet은 알림 허브와 연결된 SAS(공유 액세스 서명) 권한 부여 규칙에 대한 정보를 얻습니다.
cmdlet은 허브와 연결된 모든 규칙에 대한 정보를 반환하거나 *AuthorizationRule* 매개 변수를 포함하여 특정 규칙에 대한 정보를 얻습니다.
권한 부여 규칙은 알림 허브에 대한 액세스를 관리합니다.
권한 부여 규칙은 다른 사용 권한 수준에 따라 URI로 링크를 생성합니다.
클라이언트는 적절한 사용 권한 수준에 따라 이러한 UR 중 하나로 연결됩니다.
예를 들어 수신 권한이 있는 클라이언트는 해당 권한에 대한 URI로 연결됩니다.
**Get-AzNotificationHubAuthorizationRule** cmdlet은 알림 허브와 연결된 권한 부여 규칙에 대한 정보만 얻습니다.
허브 자체에 대한 정보를 얻습니다. Get-AzNotificationHub를 사용하세요.

## 예제

### 예제 1: 알림 허브에 할당된 모든 권한 부여 규칙에 대한 정보 얻기
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

이 명령은 ContosoNamespace 네임스페이스에서 ContosoInternalHub라는 알림 허브에 할당된 모든 권한 부여 규칙에 대한 정보를 얻습니다.
허브가 있는 네임스페이스와 허브가 할당된 리소스 그룹을 지정해야 합니다.

### 예제 2: 알림 허브에 할당된 권한 부여 규칙에 대한 정보 얻기
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

이 명령은 ContosoNamespace 네임스페이스에서 ContosoInternalHub라는 알림 허브에 할당된 모든 권한 부여 규칙에 대한 정보를 얻습니다.
이 명령은 *AuthorizationRule* 매개 변수를 사용하여 반환된 데이터를 ListenRule이라는 단일 권한 부여 규칙으로 제한합니다.

## PARAMETERS

### -AuthorizationRule
SAS 인증 규칙의 이름을 지정합니다.
이러한 규칙은 사용자가 알림 허브에 대한 액세스 유형을 결정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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
리소스 그룹은 인벤토리 관리 및 Azure 관리를 간소화하는 데 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.

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

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## 참고 사항

## 관련 링크

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubAuthorizationRule](./New-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


