---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: 944805a4883edce9354cfa372bfd30db145fc4ca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336309"
---
# Get-AzNotificationHub

## SYNOPSIS
알림 허브에 대한 정보를 얻습니다.

## 구문

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzNotificationHub** cmdlet은 지정된 네임스페이스의 알림 허브에 대한 정보를 받고 지정된 리소스 그룹에 할당됩니다.
예를 들어 네임스페이스 ContosoNamespace의 모든 알림 허브에 대한 정보를 받고 ContosoNotificationsGroup 리소스 그룹에 할당할 수 있습니다.
또는 *NotificationHub* 매개 변수를 사용하여 반환된 데이터를 특정 알림 허브에 대한 정보로 제한할 수 있습니다.
알림 허브는 해당 클라이언트에서 사용하는 iOS, Android, Windows Phone 8 및 Windows 스토어와 같은 플랫폼에 관계 없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.
이러한 허브는 개별 앱과 거의 동일하며 각 앱에는 일반적으로 자체 알림 허브가 있습니다.
이 cmdlet은 허브 자체에 대한 정보만 얻습니다.
허브의 권한 부여 규칙, 연결 문자열 및 플랫폼 알림 서비스 자격 증명에 대한 정보를 얻기 위해 Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys 및 Get-AzNotificationHubPNSCredentials와 같은 다른 cmdlet이 필요합니다.

## 예제

### 예제 1: 특정 네임스페이스의 모든 알림 허브에 대한 정보 얻기
```powershell
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

이 명령은 리소스 그룹 ContosoNotificationsGroup에 할당된 ContosoNamespace 네임스페이스의 모든 알림 허브에 대한 정보를 얻습니다.

### 예제 2

알림 허브에 대한 정보를 얻습니다. (자동Generated)

<!-- Aladdin Generated Example -->
```powershell
Get-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHub 'ContosoInternalHub' -ResourceGroup 'ContosoNotificationsGroup'
```

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
이 cmdlet이 수신하는 알림 허브의 이름을 지정합니다.
알림 허브는 해당 클라이언트에서 사용하는 플랫폼에 관계없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.

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

### Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes

## 참고 사항

## 관련 링크

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Get-AzNotificationHubListKey](./Get-AzNotificationHubListKey.md)

[Get-AzNotificationHubPNSCredential](./Get-AzNotificationHubPNSCredential.md)

[New-AzNotificationHub](./New-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


