---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496408"
---
# Get-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
알림 허브 네임스페이스와 연결된 권한 부여 규칙에 대한 정보를 얻습니다.

## 구문

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet은 알림 허브 네임스페이스와 연결된 SAS(공유 액세스 서명) 권한 부여 규칙에 대한 정보를 반환합니다.
네임스페이스와 연결된 모든 규칙에 대한 정보를 반환할 수 있습니다.
또는 *AuthorizationRule* 매개 변수를 포함하면 특정 규칙에 대한 정보를 반환할 수 있습니다.
권한 부여 규칙은 네임스페이스에 대한 액세스를 관리합니다.
이는 다른 사용 권한 수준에 따라 URIS로 링크를 만들어서 수행됩니다.
플랫폼 수준은 다음 중 하나일 수 있습니다. 
- 수신
- 보내기
- 관리 클라이언트는 적절한 사용 권한 수준에 따라 이러한 UR 중 하나로 연결됩니다.
예를 들어 수신 권한이 부여된 클라이언트는 해당 권한에 대한 URI로 연결됩니다.
이 cmdlet은 네임스페이스와 연결된 권한 부여 규칙만 얻습니다.
네임스페이스 자체에 대한 정보를 얻습니다. Get-AzNotificationHubsNamespace를 사용하세요.

## 예제

### 예제 1: 네임스페이스에 할당된 모든 권한 부여 규칙에 대한 정보 얻기
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

이 명령은 네임스페이스 ContosoNamespace 및 ContosoNotificationsGroup 리소스 그룹에 할당된 모든 권한 부여 규칙에 대한 정보를 얻습니다.

### 예제 2: 권한 부여 규칙에 대한 정보 얻기
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

이 명령은 ListenRule이라는 단일 네임스페이스 권한 부여 규칙에 대한 정보를 얻습니다.
특정 권한 부여 규칙에 대한 정보를 얻을 때 네임스페이스 및 리소스 그룹을 포함해야 합니다.

## PARAMETERS

### -AuthorizationRule
SAS 인증 규칙의 이름을 지정합니다.
이러한 규칙은 사용자가 네임스페이스에 대한 액세스 유형을 결정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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

### -Namespace
권한 부여 규칙이 할당되는 네임스페이스를 지정합니다.
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

### -ResourceGroup
권한 부여 규칙이 할당되는 리소스 그룹을 지정합니다.
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

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## 참고 사항

## 관련 링크

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


