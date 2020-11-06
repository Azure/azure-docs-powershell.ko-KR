---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
ms.openlocfilehash: 924b729ca8ba324a6f44cade48ed803b2867b6b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537040"
---
# Get-AzureRmNotificationHubListKeys

## SYNOPSIS
알림 허브 권한 부여 규칙과 연결 된 기본 및 보조 연결 문자열을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmNotificationHubListKeys [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmNotificationHubListKeys** cmdlet은 알림 허브 Sa (공유 액세스 서명) 권한 부여 규칙의 기본 및 보조 연결 문자열을 반환 합니다.

권한 부여 규칙은 허브에 대 한 사용자 권한을 관리 합니다.
각 규칙에는 기본 및 보조 연결 문자열이 포함 됩니다.
이러한 연결 문자열 (Uri)은 다음을 수행 합니다.

- 사용자를 리소스에 가리킵니다.
- 쿼리 매개 변수를 포함 하는 토큰을 포함 합니다.

이러한 매개 변수 중 하나인 시그니처는 사용자를 인증 하 고 지정 된 수준의 액세스를 제공 하는 데 사용 됩니다.

## 예제의

### 예제 1: 권한 부여 규칙에 대 한 기본 및 보조 연결 문자열 가져오기
```
PS C:\>Get-AzureRmNotificationHubListKeys -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

이 명령은 ContosoInternalHub 알림 허브에 할당 된 규칙 인 권한 부여 규칙 ListenRule에 대 한 기본 및 보조 연결 문자열을 가져옵니다.
명령에 허브 네임 스페이스 및 리소스 그룹이 포함 되어야 합니다.

## 변수

### -AuthorizationRule
SA (공유 액세스 서명) 인증 규칙의 이름을 지정 합니다.
이러한 규칙은 사용자가 알림 허브에 대해 갖는 액세스 유형을 결정 합니다.

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

### -Namespace
알림 허브가 할당 된 네임 스페이스를 지정 합니다.

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
이 cmdlet이 권한 부여 규칙을 할당 하는 알림 허브를 지정 합니다.
알림 허브는 해당 클라이언트에서 사용 하는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.

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

### Microsoft. 관리.. i g m. 목록 키

## 상속자

## 관련 링크

[Get-AzureRmNotificationHubAuthorizationRules](./Get-AzureRmNotificationHubAuthorizationRules.md)


