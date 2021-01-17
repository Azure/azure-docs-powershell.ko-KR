---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385022"
---
# Set-AzNotificationHubsNamespace

## SYNOPSIS
알림 허브 네임스페이스에 대한 속성 값을 설정합니다.

## 구문

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Set-AzNotificationHubsNamespace** cmdlet은 기존 알림 허브 네임스페이스의 속성 값을 설정합니다.
네임스페이스는 알림 허브를 구성하고 관리하는 데 도움이 되는 논리적 컨테이너입니다.
알림 허브 네임스페이스가 하나 이상 있어야 합니다.
또한 모든 알림 허브에는 할당된 네임스페이스가 있어야 합니다.
이 cmdlet은 네임스페이스를 활성화하고 사용하지 않도록 설정하는 데 주로 사용됩니다.
네임스페이스를 사용하지 않도록 설정하면 사용자는 네임스페이스의 알림 허브에 연결할 수 없으며 관리자가 해당 허브를 사용하여 푸시 알림을 보낼 수 없습니다.
비활성화된 네임스페이스를 다시 사용하도록 설정하려면 이 cmdlet을 사용하여 네임스페이스의 **상태** 속성을 활성으로 설정합니다.
또한 이 cmdlet을 사용하여 네임스페이스를 중요로 태그를 지정할 수도 있습니다.
이렇게 하면 네임스페이스가 삭제되지 않습니다.
중요한 네임스페이스를 제거하려면 먼저 중요 태그를 제거해야 합니다.

## 예제

### 예제 1: 네임스페이스 비활성화
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

이 명령은 미국 서부 데이터 센터에 있는 ContosoPartners라는 네임스페이스를 사용하지 않도록 설정하고 ContosoNotificationsGroup 리소스 그룹에 할당합니다.

### 예제 2: 네임스페이스 사용
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

이 명령은 미국 서부 데이터 센터에 있으며 ContosoNotificationsGroup 리소스 그룹에 할당된 ContosoPartners라는 네임스페이스를 사용할 수 있습니다.

## PARAMETERS

### -Critical
네임스페이스가 중요한 네임스페이스인지 여부를 나타냅니다.
중요한 네임스페이스는 삭제할 수 없습니다.
중요한 네임스페이스를 삭제하려면 네임스페이스를 중요하지 않은 것으로 표시하려면 이 속성의 값을 False로 설정해야 합니다.

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

### -Force
확인을 요청하지 않습니다.

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

### -Location
네임스페이스를 호스트하는 데이터 센터의 표시 이름을 지정합니다.
이 매개 변수를 유효한 모든 Azure 위치로 설정할 수 있습니다. 최적의 성능을 위해 대부분의 사용자 근처에 있는 데이터 센터를 사용하는 것이 좋습니다.
Azure 위치의 최신 목록을 얻습니다. 다음 명령을 실행합니다. `Get-AzLocation | Select-Object DisplayName`

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
이 cmdlet이 수정하는 네임스페이스를 지정합니다.
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
네임스페이스가 할당되는 리소스 그룹을 지정합니다.
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

### -State
네임스페이스의 현재 상태를 지정합니다.
이 매개 변수에 허용되는 값은 Active 및 Disabled입니다.

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

### -Tag
Azure 항목을 분류하고 구성하는 데 사용할 수 있는 이름-값 쌍을 지정합니다.
태그는 키워드와 유사하게 작동하며 배포 전반에서 작동됩니다.
예를 들어 Department:IT 태그를 사용하여 모든 항목을 검색하는 경우 검색은 항목 유형, 위치 또는 리소스 그룹과 같은 항목에 관계없이 해당 태그가 있는 모든 Azure 항목을 반환합니다.
개별 태그는 이름과 값(선택 사항)의 두 부분으로 *구성됩니다.* 
예를 들어 Department:IT에서 태그 이름은 Department, 태그 값은 IT입니다.
태그를 추가하기 위해 이와 유사한 해시 테이블 구문을 사용하여 CalendarYear:2016: -Tags @{Name="CalendarYear"라는 태그를 만듭니다. Value="2016"} 동일한 명령에 여러 태그를 추가하기 위해 콤마를 사용하여 개별 태그를 구분합니다. -Tag @{Name="CalendarYear"; Value="2016"}, @{Name="FiscalYear"; Value="2017"}

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

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState

### System.Boolean

### System.Collections.Hashtable

## 출력

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## 참고 사항

## 관련 링크

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)


