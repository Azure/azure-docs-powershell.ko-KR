---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: b6ece0370642d5ef0b913c96d3b817834b204e52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536739"
---
# Get-AzureRmNotificationHubAuthorizationRules

## SYNOPSIS
알림 허브에 연결 된 권한 부여 규칙에 대 한 정보를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureRmNotificationHubAuthorizationRules** cmdlet은 알림 허브에 연결 된 SAS (공유 액세스 서명) 권한 부여 규칙에 대 한 정보를 가져옵니다.
Cmdlet은 허브에 연결 된 모든 규칙에 대 한 정보를 반환 하 고, *Authorizationrule* 매개 변수를 포함 하 여 특정 규칙에 대 한 정보를 가져옵니다.

권한 부여 규칙은 알림 허브에 대 한 액세스를 관리 합니다.
권한 부여 규칙은 다양 한 사용 권한 수준에 따라 URI로 링크를 만듭니다.
클라이언트는 적절 한 사용 권한 수준에 따라 이러한 Uri 중 하나로 리디렉션됩니다.
예를 들어 Listen 권한이 있는 클라이언트는 해당 권한의 URI로 리디렉션됩니다.

**AzureRmNotificationHubAuthorizationRules** cmdlet은 알림 허브에 연결 된 권한 부여 규칙에 대 한 정보만 가져옵니다.
허브 자체에 대 한 정보를 얻으려면 Get-help를 AzureRmNotificationHub를 사용 합니다.

## 예제의

### 예제 1: 알림 허브에 할당 된 모든 권한 부여 규칙에 대 한 정보 가져오기
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

이 명령은 네임 스페이스 ContosoNamespace에서 ContosoInternalHub 이라는 알림 허브에 할당 된 모든 권한 부여 규칙에 대 한 정보를 가져옵니다.
허브가 있는 네임 스페이스와 허브가 할당 된 리소스 그룹을 지정 해야 합니다.

### 예제 2: 알림 허브에 할당 된 권한 부여 규칙에 대 한 정보 가져오기
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

이 명령은 네임 스페이스 ContosoNamespace에서 ContosoInternalHub 이라는 알림 허브에 할당 된 모든 권한 부여 규칙에 대 한 정보를 가져옵니다.
이 명령은 *Authorizationrule* 매개 변수를 사용 하 여 반환 된 데이터를 ListenRule 이라는 단일 인증 규칙으로 제한 합니다.

## 변수

### -AuthorizationRule
SAS 인증 규칙의 이름을 지정 합니다.
이러한 규칙은 사용자가 알림 허브에 대해 갖는 액세스 유형을 결정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
알림 허브가 할당 된 네임 스페이스를 지정 합니다.
네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationHub
이 cmdlet이 권한 부여 규칙을 할당 하는 알림 허브를 지정 합니다.
알림 허브는 해당 클라이언트에서 사용 하는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.

```yaml
Type: String
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
리소스 그룹은 인벤토리 관리 및 Azure 관리를 간소화 하는 데 도움이 되는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### System.webserver. List ' 1 [Microsoft Azure. 명령. SharedAccessAuthorizationRuleAttributes]

## 상속자

## 관련 링크

[Get-AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[새로운 AzureRmNotificationHubAuthorizationRules](./New-AzureRmNotificationHubAuthorizationRules.md)

[제거-AzureRmNotificationHubAuthorizationRules](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[Set-AzureRmNotificationHubAuthorizationRules](./Set-AzureRmNotificationHubAuthorizationRules.md)


