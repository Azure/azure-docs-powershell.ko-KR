---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 88e43b182694b50169738e0b775d9202aac15ffa
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399858"
---
# Get-AzNotificationHubsNamespaceListKey

## SYNOPSIS
알림 허브 네임스페이스 권한 부여 규칙과 연결된 기본 및 보조 연결 문자열을 얻습니다.

## 구문

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzNotificationHubsNamespaceListKey** cmdlet은 알림 허브 네임스페이스에 할당된 SAS(공유 액세스 서명) 권한 부여 규칙에 대한 기본 및 보조 연결 문자열을 반환합니다.
권한 부여 규칙은 알림 허브 네임스페이스에 대한 사용자 권한을 관리합니다.
각 규칙에는 기본 및 보조 연결 문자열이 포함됩니다.

## 예제

### 예제 1: 권한 부여 규칙에 대한 기본 및 보조 연결 문자열을 얻습니다.
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

이 명령은 ContosoNamespace 네임스페이스에 할당된 ListenRule이라는 권한 부여 규칙에 대한 기본 및 보조 연결 문자열을 반환합니다.
이 명령을 실행할 때 네임스페이스가 할당된 리소스 그룹의 이름을 포함해야 합니다.

## PARAMETERS

### -AuthorizationRule
SAS 인증 규칙의 이름을 지정합니다.
이러한 규칙은 사용자가 알림 허브에 대한 액세스 유형을 결정합니다.

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
이 cmdlet에서 얻을 연결 문자열을 포함하는 네임스페이스를 지정합니다.

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
네임스페이스가 할당된 리소스 그룹을 지정합니다.
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys

## 참고 사항

## 관련 링크

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)



