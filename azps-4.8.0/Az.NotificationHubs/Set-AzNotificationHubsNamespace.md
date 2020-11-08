---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204955"
---
# Set-AzNotificationHubsNamespace

## SYNOPSIS
알림 허브 네임 스페이스에 대 한 속성 값을 설정 합니다.

## 구문과

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**Set-AzNotificationHubsNamespace** cmdlet은 기존 알림 허브 네임 스페이스의 속성 값을 설정 합니다.
네임 스페이스는 알림 허브를 구성 하 고 관리 하는 데 도움이 되는 논리적 컨테이너입니다.
적어도 하나 이상의 알림 허브 네임 스페이스가 있어야 합니다.
또한 모든 알림 허브에는 지정 된 네임 스페이스가 있어야 합니다.
이 cmdlet은 주로 네임 스페이스를 사용 하거나 사용 하지 않도록 설정 하는 데 사용 됩니다.
네임 스페이스를 사용 하지 않도록 설정 하면 사용자가 네임 스페이스의 알림 허브에 연결할 수 없으며 관리자가 해당 허브를 사용 하 여 푸시 알림을 보낼 수 없습니다.
비활성화 된 네임 스페이스를 다시 사용 하도록 설정 하려면이 cmdlet을 사용 하 여 네임 스페이스의 **State** 속성을 Active로 설정 합니다.
이 cmdlet을 사용 하 여 네임 스페이스에 중요 한 태그를 지정할 수도 있습니다.
이렇게 하면 네임 스페이스가 삭제 되지 않습니다.
중요 한 네임 스페이스를 제거 하려면 먼저 중요 한 태그를 제거 해야 합니다.

## 예제의

### 예제 1: 네임 스페이스 비활성화
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

이 명령은 ContosoPartners 라는 네임 스페이스를 사용 하지 않도록 설정 하 고 ContosoNotificationsGroup 리소스 그룹에 할당 합니다.

### 예제 2: 네임 스페이스 사용
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

이 명령은 ContosoPartners 라는 네임 스페이스를 사용 하도록 설정 하 고 ContosoNotificationsGroup 리소스 그룹에 할당 합니다.

## 변수

### -중요
네임 스페이스가 중요 한 네임 스페이스 인지 여부를 나타냅니다.
중요 한 네임 스페이스는 삭제할 수 없습니다.
중요 한 네임 스페이스를 삭제 하려면 네임 스페이스를 중요 하지 않은 것으로 표시 하기 위해이 속성의 값을 False로 설정 해야 합니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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

### -Force
확인 메시지를 표시 하지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
네임 스페이스를 호스트 하는 데이터 센터의 표시 이름을 지정 합니다.
이 매개 변수를 유효한 Azure 위치로 설정할 수 있지만, 최적의 성능을 위해서는 대다수 사용자의 근처에 있는 데이터 센터를 사용 해야 합니다.
Azure 위치를 최신 목록으로 가져오려면 다음 명령을 실행 합니다. `Get-AzLocation | Select-Object DisplayName`

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

### -Namespace
이 cmdlet이 수정 하는 네임 스페이스를 지정 합니다.
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

### -서 고 U계층
네임 스페이스의 Sku 계층

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -상태
네임 스페이스의 현재 상태를 지정 합니다.
이 매개 변수에 허용 되는 값은 Active 및 Disabled입니다.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
Azure 항목을 분류 하 고 구성 하는 데 사용할 수 있는 이름-값 쌍을 지정 합니다.
태그는 키워드와 유사 하 게 작동 하며 배포에서 작동 합니다.
예를 들어 태그 부서가 있는 모든 항목을 검색 하는 경우 항목 유형, 위치 또는 리소스 그룹과 관계 없이 해당 태그가 있는 모든 Azure 항목이 검색 결과로 반환 됩니다.
개별 태그는 *이름* 및 *값* (선택적으로)의 두 부분으로 구성 됩니다.
예를 들어 부서에서는 태그 이름이 부서이 고 tag 값은입니다.
태그를 추가 하려면 다음과 같은 해시 테이블 구문을 사용 합니다. CalendarYear (2016:-tag @ {Name = "CalendarYear")를 만듭니다. Value = "2016"} 같은 명령에 여러 태그를 추가 하려면 쉼표를 사용 하 여 개별 태그를 구분 합니다.-Tag @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "FiscalYear"; Value = "2017"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### Microsoft. Azure. NamespaceState

### 시스템 부울

### System.webserver. 컬렉션 테이블

## 출력

### Microsoft. Azure. NamespaceAttributes

## 상속자

## 관련 링크

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[새로운 AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[제거-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)


