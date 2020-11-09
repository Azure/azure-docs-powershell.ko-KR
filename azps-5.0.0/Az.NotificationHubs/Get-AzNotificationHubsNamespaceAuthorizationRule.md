---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309119"
---
# Get-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
알림 허브 네임 스페이스와 연결 된 권한 부여 규칙에 대 한 정보를 가져옵니다.

## 구문과

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzNotificationHubsNamespaceAuthorizationRule** cmdlet은 알림 허브 네임 스페이스와 관련 된 SAS (공유 액세스 서명) 권한 부여 규칙에 대 한 정보를 반환 합니다.
네임 스페이스와 관련 된 모든 규칙에 대 한 정보를 반환할 수 있습니다.
또는 *authorizationrule* 매개 변수를 포함 하 여 특정 규칙에 대 한 정보를 반환할 수 있습니다.
권한 부여 규칙은 네임 스페이스에 대 한 액세스를 관리 합니다.
이 작업은 다양 한 사용 권한 수준에 따라 Uri로 링크를 만들어 수행 됩니다.
플랫폼 수준은 다음 중 하나가 될 수 있습니다. 
- 듣기
- 보내기
- 클라이언트 관리는 적절 한 사용 권한 수준에 따라 이러한 Uri 중 하나로 향합니다.
예를 들어 Listen 권한이 지정 된 클라이언트는 해당 사용 권한에 대 한 URI로 전송 됩니다.
이 cmdlet은 네임 스페이스와 관련 된 권한 부여 규칙만 가져옵니다.
네임 스페이스 자체에 대 한 정보를 얻으려면 Get-AzNotificationHubsNamespace를 사용 합니다.

## 예제의

### 예제 1: 네임 스페이스에 할당 된 모든 권한 부여 규칙에 대 한 정보 가져오기
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

이 명령은 네임 스페이스 ContosoNamespace 및 ContosoNotificationsGroup 리소스 그룹에 모두 할당 된 모든 권한 부여 규칙에 대 한 정보를 가져옵니다.

### 예제 2: 권한 부여 규칙에 대 한 정보 가져오기
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

이 명령은 ListenRule 이라는 단일 네임 스페이스 권한 부여 규칙에 대 한 정보를 가져옵니다.
특정 권한 부여 규칙에 대 한 정보를 가져올 때는 네임 스페이스와 리소스 그룹을 포함 해야 합니다.

## 변수

### -AuthorizationRule
SAS 인증 규칙의 이름을 지정 합니다.
이러한 규칙은 네임 스페이스에 대 한 사용자의 액세스 유형을 결정 합니다.

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

### -ResourceGroup
권한 부여 규칙이 할당 되는 리소스 그룹을 지정 합니다.
리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Microsoft. Azure. 명령. SharedAccessAuthorizationRuleAttributes

## 상속자

## 관련 링크

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[새로운 AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[제거-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


