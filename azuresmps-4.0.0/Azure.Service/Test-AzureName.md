---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045937"
---
# Test-AzureName

## SYNOPSIS
Microsoft Azure 클라우드 서비스 이름, 저장소 서비스 이름 또는 서비스 버스 네임 스페이스 이름이 있는지 여부를 테스트 합니다.

## 구문과

### Services
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### 용량
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServiceBusNamespace
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### 웹 사이트
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이름이 있으면 cmdlet이 $True를 반환 합니다.
이름이 없는 경우 $False 반환 합니다.

## 예제의

### 예제 1
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

이 명령을 테스트 하 여 "MyNameService1"이 기존 Microsoft Azure 클라우드 서비스 이름 인지 확인 합니다.

### 예제 2
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

이 명령은 "mystorename1"이 기존 Microsoft Azure 저장소 서비스 이름 인지 확인 합니다.

### 예제 3
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

이 명령을 테스트 하 여 "mynamespace"이 기존 Microsoft Azure service bus 네임 스페이스 이름 인지 확인 합니다.

## 변수

### -이름
테스트할 서비스 또는 저장소 계정의 이름을 지정 합니다.

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

### -서비스
기존 서비스 계정을 테스트 하도록 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceBusNamespace
기존 service bus 네임 스페이스를 테스트 하도록 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -저장소
기존 저장소 계정을 테스트 하도록 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -웹 사이트
기존 웹 사이트를 테스트 하도록 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
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
* 노드 개발자, php-개발자, python-개발자

## 관련 링크

