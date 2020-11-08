---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046309"
---
# Get-AzureService

## SYNOPSIS
현재 구독에 대 한 클라우드 서비스에 대 한 정보가 포함 된 개체를 반환 합니다.

## 구문과

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**Get-AzureService** cmdlet은 현재 구독과 연결 된 모든 Azure 클라우드 서비스가 포함 된 list 개체를 반환 합니다.
*ServiceName* 매개 변수를 지정 하면 **Get-azureservice** 는 일치 하는 서비스에 대 한 정보만 반환 합니다.

## 예제의

### 예제 1: 모든 서비스에 대 한 정보 가져오기
```
PS C:\> Get-AzureService
```

이 명령은 현재 구독과 연결 된 모든 Azure 서비스에 대 한 정보를 포함 하는 개체를 반환 합니다.

### 예제 2: 지정 된 서비스에 대 한 정보 가져오기
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

이 명령은 $MySvc 서비스에 대 한 정보를 반환 합니다.

### 예제 3: 사용 가능한 메서드 및 속성 표시
```
PS C:\> Get-AzureService | Get-Member
```

이 명령은 **가져오기-AzureService** cmdlet에서 사용할 수 있는 속성 및 메서드를 표시 합니다.

## 변수

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
정보 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -ServiceName
정보를 반환할 서비스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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

### HostedServiceContext

## 상속자

## 관련 링크

[새-AzureService](./New-AzureService.md)

[Set AzureService](./Set-AzureService.md)


