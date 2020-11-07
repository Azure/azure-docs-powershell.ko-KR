---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710943"
---
# Test-AzureRmServiceBusName

## SYNOPSIS
지정 된 네임 스페이스 이름 사용 가능 여부를 확인 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## 설명은
네임 스페이스 이름의 **AzureRmServiceBusName** Cmdlet 검사 사용 가능성

## 예제의

### 예제 1
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### 예제 2
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### 예제 3
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

네임 스페이스 이름 사용 가능성에 대 한 상태를 반환 합니다.

## 변수

### -Namespace
ServiceBus 네임 스페이스 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### -Namespace
 System. 문자열

## 출력

### [ServiceBus, CheckNameAvailabilityResultAttributes, ServiceBus, Version = 0.1.0.0, Culture = 중립, PublicKeyToken = null] 등의 명령을 표시 합니다.

### 예제 1
이름 사용 가능한 이유 메시지
------------- ------ -------
         True   None

### 예제 2
이름 사용 가능한 이유 메시지
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### 예제 3
이름 사용 가능한 이유 메시지
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## 상속자

## 관련 링크
