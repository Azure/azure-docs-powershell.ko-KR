---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3d0e604d3984a40acde02fb1f977e2922ae2d1d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495068"
---
# Get-AzNotificationHubsNamespace

## SYNOPSIS
알림 허브 네임스페이스에 대한 정보를 얻습니다.

## 구문

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzNotificationHubsNamespace** cmdlet은 알림 허브 네임스페이스에 대한 정보를 얻습니다.
이 cmdlet은 모든 네임스페이스에 대한 정보, 지정된 리소스 그룹에 할당된 네임스페이스에 대한 정보를 제공하는 옵션을 제공합니다. 또는 특정 네임스페이스에 대한 정보를 반환합니다.
네임스페이스는 알림 허브를 구성하고 관리하는 데 도움이 되는 논리적 컨테이너입니다.
알림 허브 네임스페이스가 하나 이상 있어야 합니다. 모든 알림 허브를 네임스페이스에 할당해야 합니다.
단일 네임스페이스는 여러 허브를 사용할 수 있습니다. 즉, 조직에 하나의 네임스페이스만 필요할 수 있습니다.
그러나 허브를 보다 효율적으로 구성하거나 특정 개인에게 선택한 허브 하위 집합을 관리할 수 있는 권한을 부여하기 위해 여러 네임스페이스를 사용할 수도 있습니다.
**Get-AzNotificationHubsNamespace** cmdlet은 네임스페이스 자체에 대한 기본 정보를 반환합니다.
네임스페이스와 연결된 권한 부여 규칙에 대한 정보를 얻습니다. Get-AzNotificationHubsNamespaceAuthorizationRules를 사용하세요.

## 예제

### 예제 1: 모든 알림 허브 네임스페이스에 대한 정보 얻기
```
PS C:\>Get-AzNotificationHubsNamespace
```

이 명령은 모든 알림 허브 네임스페이스에 대한 정보를 반환합니다.

### 예제 2: 단일 알림 허브 네임스페이스에 대한 정보 얻기
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

이 명령은 단일 알림 허브 네임스페이스인 ContosoNamespace에 대한 정보를 얻습니다.

### 예제 3: 특정 네임스페이스에 할당된 모든 알림 허브에 대한 정보 얻기
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

이 명령은 리소스 그룹에 할당된 모든 알림 허브 네임스페이스에 대한 정보를 얻습니다.

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
네임스페이스에 대한 고유한 이름을 지정합니다.
네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
네임스페이스가 할당되는 리소스 그룹을 지정합니다.
리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## 참고 사항

## 관련 링크

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


