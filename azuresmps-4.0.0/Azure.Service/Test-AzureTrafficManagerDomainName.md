---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045935"
---
# Test-AzureTrafficManagerDomainName

## SYNOPSIS
도메인 이름을 Traffic Manager 프로필로 사용할 수 있는지 여부를 확인 합니다.

## 구문과

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureTrafficManagerDomainName** cmdlet은 도메인 이름을 Microsoft Azure Traffic Manager 프로필로 사용할 수 있는지 여부를 확인 합니다.
도메인 이름을 사용할 수 있는 경우이 cmdlet은 $True 값을 반환 합니다.

## 예제의

### 예제 1: 도메인 이름을 사용할 수 있는지 확인
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

이 명령은 도메인 이름 ContosoApp.trafficmanager.net을 Traffic Manager 프로필로 사용할 수 있는지 여부를 확인 합니다.

## 변수

### -DomainName
테스트할 도메인 이름을 지정 합니다.
다음 문자열을 포함 해야 합니다. 

trafficmanager.net

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다. 프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### 시스템 부울
이 cmdlet은 $True 또는 $False를 생성 합니다.
도메인 이름을 사용할 수 있는 경우이 cmdlet은 $True 값을 반환 합니다.

## 상속자

## 관련 링크

