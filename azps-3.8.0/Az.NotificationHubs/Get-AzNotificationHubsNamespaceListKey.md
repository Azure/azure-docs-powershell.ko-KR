---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 90e617f35442470cef2d11c2de032679698ea167
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878926"
---
# Get-AzNotificationHubsNamespaceListKey

## SYNOPSIS
알림 허브 네임 스페이스 권한 부여 규칙과 연결 된 기본 및 보조 연결 문자열을 가져옵니다.

## 구문과

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzNotificationHubsNamespaceListKey** cmdlet은 알림 허브 네임 스페이스에 할당 된 SAS (공유 액세스 서명) 권한 부여 규칙에 대 한 기본 및 보조 연결 문자열을 반환 합니다.
권한 부여 규칙은 알림 허브 네임 스페이스에 대 한 사용자 권한을 관리 합니다.
각 규칙에는 기본 및 보조 연결 문자열이 포함 됩니다.

## 예제의

### 예제 1: 권한 부여 규칙에 대 한 기본 및 보조 연결 문자열 가져오기
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

이 명령은 ContosoNamespace 네임 스페이스에 할당 된 ListenRule 이라는 권한 부여 규칙에 대 한 기본 및 보조 연결 문자열을 반환 합니다.
이 명령을 실행할 때는 네임 스페이스에 할당 된 리소스 그룹의 이름을 포함 해야 합니다.

## 변수

### -AuthorizationRule
SAS 인증 규칙의 이름을 지정 합니다.
이러한 규칙은 사용자가 알림 허브에 대해 갖는 액세스 유형을 결정 합니다.

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
이 cmdlet이 가져오는 연결 문자열을 포함 하는 네임 스페이스를 지정 합니다.

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
네임 스페이스를 할당할 리소스 그룹을 지정 합니다.
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

### Microsoft. 관리.. i g m. 목록 키

## 상속자

## 관련 링크

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Get-AzNotificationHubsNamespaceAuthorizationRules](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)


