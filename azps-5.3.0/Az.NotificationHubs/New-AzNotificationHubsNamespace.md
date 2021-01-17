---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491750"
---
# New-AzNotificationHubsNamespace

## SYNOPSIS
알림 허브 네임스페이스를 만듭니다.

## 구문

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**New-AzNotificationHubsNamespace** cmdlet은 알림 허브 네임스페이스를 만듭니다.
네임스페이스는 알림 허브를 구성하고 관리하는 데 도움이 되는 논리적 컨테이너입니다.
알림 허브 네임스페이스가 하나 이상 있어야 합니다.
단일 네임스페이스는 여러 허브를 사용할 수 있습니다.
여러 네임스페이스를 사용하여 허브를 구성하거나 특정 개인에게 허브의 선택한 하위 집합을 관리할 수 있는 권한을 부여할 수 있습니다.
네임스페이스를 만들 경우 네임스페이스에 대한 고유한 이름을 지정해야 합니다. 네임스페이스가 있는 데이터 센터를 지정합니다. 네임스페이스를 할당할 리소스 그룹을 지정합니다.
네임스페이스를 만든 후 New-AzNotificationHubsNamespaceAuthorizationRules cmdlet을 사용하여 해당 네임스페이스에 권한 부여 규칙을 할당할 수 있습니다.
권한 부여 규칙은 네임스페이스에 대한 사용 권한을 관리하는 데 사용됩니다.

## 예제

### 예제 1: 알림 허브 만들기
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

이 명령은 ContosoPartners라는 알림 허브를 만듭니다.
네임스페이스는 미국 서부 데이터 센터에 있으며 ContosoNotificationsGroup 리소스 그룹에 할당됩니다.

### 예제 2: 태그가 있는 알림 허브 만들기
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

이 명령은 ContosoPartners라는 알림 허브를 만듭니다.
네임스페이스는 미국 서부 데이터 센터에 있으며 ContosoNotificationsGroup 리소스 그룹에 할당됩니다.
또한 이 명령은 Audience 이름과 PartnerOrganizations 값으로 태그를 만들고 네임스페이스에 할당합니다.
이렇게 하면 대상 태그가 PartnerOrganizations로 설정된 항목에 대해 필터링할 때 네임스페이스가 표시될 수 있습니다.

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

### -Location
네임스페이스를 호스트할 데이터 센터의 표시 이름을 지정합니다.
이 매개 변수를 유효한 위치로 설정할 수 있습니다. 최적의 성능을 위해 대부분의 사용자 근처에 있는 데이터 센터를 사용할 수 있습니다.

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
새 네임스페이스의 이름을 지정합니다.
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

### -ResourceGroup
네임스페이스를 할당할 리소스 그룹을 지정합니다.
리소스 그룹은 인벤토리 관리 및 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.

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

### -SkuTier
네임스페이스의 SKU 계층

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

### -Tag
Azure 항목을 분류하고 구성하는 데 사용할 수 있는 이름-값 쌍을 지정합니다.
태그는 키워드와 유사하게 작동하며 배포 전반에서 작동됩니다.
예를 들어 Department:IT 태그를 사용하여 모든 항목을 검색하는 경우 검색은 항목 유형, 위치 또는 리소스 그룹과 같은 항목에 관계없이 해당 태그가 있는 모든 Azure 항목을 반환합니다.
개별 태그는 이름 및 선택적으로 *값의* 두 부분으로 *구성됩니다.*
예를 들어 Department:IT에서 태그 이름은 Department, 태그 값은 IT입니다.
태그를 추가하기 위해 이와 유사한 해시 테이블 구문을 사용하여 CalendarYear:2016 태그를 만듭니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

### System.Collections.Hashtable

## 출력

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## 참고 사항

## 관련 링크

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


