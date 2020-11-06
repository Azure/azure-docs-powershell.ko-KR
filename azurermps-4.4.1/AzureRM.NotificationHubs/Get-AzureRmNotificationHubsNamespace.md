---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b1217a9ca49d81cf084d97983e8ec5ebd99ed84a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529251"
---
# Get-AzureRmNotificationHubsNamespace

## SYNOPSIS
알림 허브 네임 스페이스에 대 한 정보를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmNotificationHubsNamespace Cmdlet은** 알림 허브 네임 스페이스에 대 한 정보를 가져옵니다.
이 cmdlet은 모든 네임 스페이스, 즉 지정 된 리소스 그룹에 할당 된 네임 스페이스에 대 한 정보를 가져올 수 있는 옵션을 제공 합니다. 특정 네임 스페이스에 대 한 정보를 반환 합니다.

네임 스페이스는 알림 허브를 구성 하 고 관리 하는 데 도움이 되는 논리적 컨테이너입니다.
하나 이상의 알림 허브 네임 스페이스가 있어야 합니다. 모든 알림 허브는 네임 스페이스에 할당 되어야 합니다.
단일 네임 스페이스는 조직에서 하나의 네임 스페이스만 필요할 수 있다는 것을 의미 하는 여러 허브를 배치할 수 있습니다.
그러나 허브를 더 효과적으로 구성 하거나 특정 개인에 게 선택한 허브 하위 집합을 관리할 수 있는 권한을 부여 하기 위해 여러 네임 스페이스를 사용할 수도 있습니다.

**Get-AzureRmNotificationHubsNamespace** cmdlet은 네임 스페이스 자체에 대 한 기본 정보를 반환 합니다.
네임 스페이스에 연결 된 권한 부여 규칙에 대 한 정보를 얻으려면 Get-AzureRmNotificationHubsNamespaceAuthorizationRules를 사용 합니다.

## 예제의

### 예제 1: 모든 알림 허브 네임 스페이스에 대 한 정보 가져오기
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

이 명령은 모든 알림 허브 네임 스페이스에 대 한 정보를 반환 합니다.

### 예제 2: 단일 알림 허브 네임 스페이스에 대 한 정보 가져오기
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

이 명령은 단일 알림 허브 네임 스페이스에 대 한 정보를 가져옵니다: ContosoNamespace.

### 예제 3: 특정 네임 스페이스에 할당 된 모든 알림 허브에 대 한 정보 가져오기
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

이 명령은 리소스 그룹 ContosoNotificationsGroup에 할당 된 모든 알림 허브 네임 스페이스에 대 한 정보를 가져옵니다.

## 변수

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### NamespaceAttributes의 목록 ' 1 [Microsoft. h t e.]

## 상속자

## 관련 링크

[Get-AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[새로운 AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[제거-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Set-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


