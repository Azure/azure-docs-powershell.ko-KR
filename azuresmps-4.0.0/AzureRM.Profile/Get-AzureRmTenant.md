---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523396"
---
# Get-AzureRmTenant

## SYNOPSIS
현재 사용자에 대해 권한이 있는 테 넌 트를 가져옵니다.

## 구문과

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## 설명은
Get-AzureRmTenant cmdlet은 현재 사용자에 대해 승인 된 테 넌 트를 가져옵니다.

## 예제의

### 예제 1: 모든 테 넌 트 가져오기
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

이 예제에서는 Azure 계정의 모든 권한이 부여 된 테 넌 트를 가져오는 방법을 보여 줍니다.

### 예제 2: 특정 테 넌 트 가져오기
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

이 예제에서는 Azure 계정에 대해 권한이 부여 된 특정 테 넌 트를 가져오는 방법을 보여 줍니다.

## 변수

### -TenantId
이 cmdlet이 가져오는 테 넌 트의 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### PSAzureTenant
이 cmdlet은 현재 계정에 대해 승인 된 테 넌 트 ID 및 연결 된 도메인 정보를 반환 합니다.

## 상속자

## 관련 링크

