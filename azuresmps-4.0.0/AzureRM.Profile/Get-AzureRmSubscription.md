---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 13dd14f59b28e3b5730f207c675771e1275392d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523399"
---
# Get-AzureRmSubscription

## SYNOPSIS
현재 계정이 액세스할 수 있는 구독을 가져옵니다.

## 구문과

### ListByIdInTenant (기본값)
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [<CommonParameters>]
```

### ListByNameInTenant
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [<CommonParameters>]
```

## 설명은
Get-AzureRmSubscription cmdlet은 현재 계정이 액세스할 수 있는 구독에 대 한 구독 ID, 구독 이름 및 홈 테 넌 트를 가져옵니다.

## 예제의

### 예제 1: 모든 테 넌 트의 모든 구독 가져오기
```
PS C:\>Get-AzureRmSubscription -All

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

이 명령은 현재 계정에 대해 권한이 있는 모든 테 넌 트의 모든 구독을 가져옵니다.

### 예제 2: 특정 테 넌 트에 대 한 모든 구독 가져오기
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

지정 된 테 넌 트에서 현재 계정에 대해 권한이 있는 모든 구독을 나열 합니다.

### 예제 3: 현재 테 넌 트의 모든 구독 가져오기
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

이 명령은 현재 테 넌 트에서 현재 사용자에 대해 권한이 부여 된 모든 구독을 가져옵니다.

### 예제 4: 특정 구독을 사용 하도록 현재 컨텍스트 변경
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

이 명령은 지정 된 구독을 가져온 다음 현재 컨텍스트를 사용 하도록 설정 합니다.
이 세션의 모든 후속 cmdlet은 기본적으로 새 구독 (Contoso 구독 1)을 사용 합니다.

## 변수

### -SubscriptionId
가져올 구독의 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
가져올 구독의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantId
가져올 구독이 포함 된 테 넌 트의 ID를 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### PSAzureSubscription

## 상속자

## 관련 링크

