---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7B2CDFF-D9A2-48C7-B331-132A6A6843CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 10fdb8920164857b42ac57a3c989417c2a967ab9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045614"
---
# Get-AzureSBAuthorizationRule

## SYNOPSIS
서비스 버스 권한 부여 규칙을 가져옵니다.


## 구문과

### EntitySAS
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### NamespaceSAS
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
서비스 버스 권한 부여 규칙을 가져옵니다.

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## 예제의

### 예제 1: 네임 스페이스 수준에서 권한 부여 규칙 가져오기
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace
```

MyNamespace에서 사용 가능한 모든 권한 부여 규칙을 가져옵니다.

### 예제 2: 큐에 대 한 권한 부여 규칙 가져오기
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

MyNamespace의 MyEntity 큐에서 사용 가능한 모든 권한 부여 규칙을 가져옵니다.

### 예제 3: 이름으로 권한 부여 규칙 가져오기
```
PS C:\> Get-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

MyNamespace 수준에서 MyRule 이라는 권한 부여 규칙을 가져옵니다.

### 예제 4: 권한으로 권한 부여 규칙 가져오기
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -Permission $("Send")
```

네임 스페이스 수준에 대 한 보내기 권한이 있는 모든 권한 부여 규칙을 가져옵니다.

## 변수

### -EntityName
규칙을 적용할 엔터티 이름입니다.

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EntityType
엔터티 형식 (큐, 주제, 릴레이, NotificationHub).

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
고유한 인증 규칙 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
권한 부여 규칙을 적용할 네임 스페이스 이름입니다.
EntityName을 제공 하지 않으면 규칙은 네임 스페이스 수준에 있게 됩니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -사용 권한
필터링 할 승인 권한 (보내기, 관리, 수신 대기)입니다.
정확한 일치를 사용 합니다.

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

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

## 상속자

## 관련 링크

[새로운 AzureSBAuthorizationRule](./New-AzureSBAuthorizationRule.md)

[제거-AzureSBAuthorizationRule](./Remove-AzureSBAuthorizationRule.md)

[Set-AzureSBAuthorizationRule](./Set-AzureSBAuthorizationRule.md)


