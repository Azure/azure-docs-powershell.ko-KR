---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523403"
---
# Get-AzureRmContext

## SYNOPSIS
Azure Resource Manager 요청을 인증 하는 데 사용 되는 메타 데이터를 가져옵니다.

## 구문과

```
Get-AzureRmContext [<CommonParameters>]
```

## 설명은
Get-AzureRmContext cmdlet은 Azure Resource Manager 요청을 인증 하는 데 사용 된 현재 메타 데이터를 가져옵니다.

이 cmdlet은 Active Directory 계정, Active Directory 테 넌 트, Azure 구독, 대상 Azure 환경을 가져옵니다.
Azure resource manager cmdlet은 Azure Resource Manager 요청을 수행할 때 기본적으로 이러한 설정을 사용 합니다.

## 예제의

### 예제 1: 현재 컨텍스트 가져오기
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

이 예제에서는 AzureRmAccount를 사용 하 여 Azure 구독이 있는 계정에 로그인 하 고, 이제 Get-AzureRmContext를 호출 하 여 현재 세션의 컨텍스트를 가져옵니다.

## 변수

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### PSAzureContext
이 cmdlet은 Azure Resource Manager cmdlet에 사용 되는 계정, 테 넌 트 및 구독을 반환 합니다.

## 상속자

## 관련 링크

[Set-AzureRMContext]()

