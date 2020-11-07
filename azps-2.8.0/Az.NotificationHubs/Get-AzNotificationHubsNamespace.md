---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: dbb475402ef4068f893cd7d444b5357bf1707578
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872010"
---
# Get-AzNotificationHubsNamespace

## SYNOPSIS
알림 허브 네임 스페이스에 대 한 정보를 가져옵니다.

## 구문과

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzNotificationHubsNamespace Cmdlet은** 알림 허브 네임 스페이스에 대 한 정보를 가져옵니다.
이 cmdlet은 모든 네임 스페이스, 즉 지정 된 리소스 그룹에 할당 된 네임 스페이스에 대 한 정보를 가져올 수 있는 옵션을 제공 합니다. 특정 네임 스페이스에 대 한 정보를 반환 합니다.
네임 스페이스는 알림 허브를 구성 하 고 관리 하는 데 도움이 되는 논리적 컨테이너입니다.
하나 이상의 알림 허브 네임 스페이스가 있어야 합니다. 모든 알림 허브는 네임 스페이스에 할당 되어야 합니다.
단일 네임 스페이스는 조직에서 하나의 네임 스페이스만 필요할 수 있다는 것을 의미 하는 여러 허브를 배치할 수 있습니다.
그러나 허브를 더 효과적으로 구성 하거나 특정 개인에 게 선택한 허브 하위 집합을 관리할 수 있는 권한을 부여 하기 위해 여러 네임 스페이스를 사용할 수도 있습니다.
**Get-AzNotificationHubsNamespace** cmdlet은 네임 스페이스 자체에 대 한 기본 정보를 반환 합니다.
네임 스페이스에 연결 된 권한 부여 규칙에 대 한 정보를 얻으려면 Get-AzNotificationHubsNamespaceAuthorizationRules를 사용 합니다.

## 예제의

### 예제 1: 모든 알림 허브 네임 스페이스에 대 한 정보 가져오기
```
PS C:\>Get-AzNotificationHubsNamespace
```

이 명령은 모든 알림 허브 네임 스페이스에 대 한 정보를 반환 합니다.

### 예제 2: 단일 알림 허브 네임 스페이스에 대 한 정보 가져오기
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

이 명령은 단일 알림 허브 네임 스페이스에 대 한 정보를 가져옵니다: ContosoNamespace.

### 예제 3: 특정 네임 스페이스에 할당 된 모든 알림 허브에 대 한 정보 가져오기
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

이 명령은 리소스 그룹 ContosoNotificationsGroup에 할당 된 모든 알림 허브 네임 스페이스에 대 한 정보를 가져옵니다.

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

### -Namespace
네임 스페이스에 대 한 고유한 이름을 지정 합니다.
네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.

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
네임 스페이스를 할당할 리소스 그룹을 지정 합니다.
리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Microsoft. Azure. NamespaceAttributes

## 상속자

## 관련 링크

[Get-AzNotificationHubsNamespaceAuthorizationRules](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)

[새로운 AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[제거-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


