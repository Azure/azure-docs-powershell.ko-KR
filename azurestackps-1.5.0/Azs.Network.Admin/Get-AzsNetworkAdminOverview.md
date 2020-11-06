---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523347"
---
# Get-AzsNetworkAdminOverview

## SYNOPSIS
네트워크 리소스 공급자의 상태에 대 한 개요를 확인 하세요.

## 구문과

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## 설명은
네트워크 리소스 공급자의 상태에 대 한 개요를 확인 하세요. 개별 속성은 리소스 사용 및 구성 요소의 상태에 대 한 자세한 개수를 제공 합니다.

## 예제의

### --------------------------예제 1--------------------------
```
Get-AzsNetworkAdminOverview
```

네트워크 관리 개요를 확인 하세요.

### --------------------------예제 2--------------------------
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

공용 ip 주소 사용을 가져옵니다.

## 변수

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### Microsoft AzureStack. 관리자. 관리 모델 개요

## 상속자

## 관련 링크

