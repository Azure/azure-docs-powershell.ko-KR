---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/get-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 8f9cfda051542327fdb6175da081c99e6b8b6b3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526495"
---
# Get-AzureRmSubscriptionDefinition

## SYNOPSIS
구독 정의를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 구독 정의를 가져옵니다.
```
Get-AzureRmSubscriptionDefinition
```

## 예제의

### 예제 1
```
PS C:\> Get-AzureRmSubscriptionDefinition

Name                    : MyProdSubscription1
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyProdSubscription1
OfferType               : MS-AZR-0017P

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

모든 구독 정의를 가져옵니다.

### 예제 2
```
PS C:\> Get-AzureRmSubscriptionDefinition -Name MyProdSubscription2

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

이름 MyProdSubscription2를 사용 하 여 구독 정의를 가져옵니다.

## 변수

### -이름
검색할 구독 정의의 이름입니다.

```yaml
Type: String
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

### 않아야

## 출력

### System.webserver. List ' 1 [[Microsoft Azure.]. e n t 구독 정의, Microsoft Azure. 명령인 정의, Version = 0.1.0.0, Culture = 중립, PublicKeyToken = null]]

## 상속자

## 관련 링크

