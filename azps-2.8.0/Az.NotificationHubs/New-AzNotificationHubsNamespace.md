---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: a9675f2473488d1415a83ae0454a3841cd10d589
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872538"
---
# New-AzNotificationHubsNamespace

## SYNOPSIS
알림 허브 네임 스페이스를 만듭니다.

## 구문과

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**새 AzNotificationHubsNamespace** cmdlet은 알림 허브 네임 스페이스를 만듭니다.
네임 스페이스는 알림 허브를 구성 하 고 관리 하는 데 도움이 되는 논리적 컨테이너입니다.
적어도 하나 이상의 알림 허브 네임 스페이스가 있어야 합니다.
단일 네임 스페이스는 여러 허브를 배치할 수 있습니다.
여러 네임 스페이스를 사용 하 여 허브를 구성 하거나 특정 개인에 게 허브의 선택 된 하위 집합을 관리 하기 위한 권한을 부여할 수 있습니다.
네임 스페이스를 만들려면 네임 스페이스에 대 한 고유한 이름을 지정 해야 합니다. 네임 스페이스의 위치를 지정할 데이터 센터를 지정 합니다. 네임 스페이스에 할당할 리소스 그룹을 지정 합니다.
네임 스페이스를 만든 후에는 New-AzNotificationHubsNamespaceAuthorizationRules cmdlet을 사용 하 여 해당 네임 스페이스에 권한 부여 규칙을 할당할 수 있습니다.
권한 부여 규칙은 네임 스페이스에 대 한 사용 권한을 관리 하는 데 사용 됩니다.

## 예제의

### 예제 1: 알림 허브 만들기
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

이 명령은 ContosoPartners 이라는 알림 허브를 만듭니다.
네임 스페이스는 서쪽 US 데이터 센터에 위치 하 고 ContosoNotificationsGroup 리소스 그룹에 할당 됩니다.

### 예제 2: 태그를 사용 하 여 알림 허브 만들기
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

이 명령은 ContosoPartners 이라는 알림 허브를 만듭니다.
네임 스페이스는 서쪽 US 데이터 센터에 위치 하 고 ContosoNotificationsGroup 리소스 그룹에 할당 됩니다.
또한이 명령은 이름 대상과 값이 지정 된 조직으로 태그를 만들고 네임 스페이스에 할당 됩니다.
이렇게 하면 대상 그룹 태그가 있는 항목에 대해 필터링 할 때마다 네임 스페이스를 표시할 수 있습니다.

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

### -위치
네임 스페이스를 호스팅할 데이터 센터의 표시 이름을 지정 합니다.
이 매개 변수를 올바른 위치로 설정할 수 있지만 최적의 성능을 위해 대부분의 사용자에 게 있는 데이터 센터를 사용 하는 것이 좋습니다.

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
새 네임 스페이스의 이름을 지정 합니다.
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
리소스 그룹은 간단 하 게 관리 및 관리를 위한 방법으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.

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

### 태그
Azure 항목을 분류 하 고 구성 하는 데 사용할 수 있는 이름-값 쌍을 지정 합니다.
태그는 키워드와 유사 하 게 작동 하며 배포에서 작동 합니다.
예를 들어 태그 부서가 있는 모든 항목을 검색 하는 경우 항목 유형, 위치 또는 리소스 그룹과 관계 없이 해당 태그가 있는 모든 Azure 항목이 검색 결과로 반환 됩니다.
개별 태그는 *이름* , 선택적으로 *값* 등의 두 부분으로 구성 됩니다.
예를 들어 부서에서는 태그 이름이 부서이 고 tag 값은입니다.
태그를 추가 하려면 다음과 같이 태그를 만드는 해시 테이블 구문을 사용 합니다. CalendarYear: 2016:

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### System.webserver. 컬렉션 테이블

## 출력

### Microsoft. Azure. NamespaceAttributes

## 상속자

## 관련 링크

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[제거-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


