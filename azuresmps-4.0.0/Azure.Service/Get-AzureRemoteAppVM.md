---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D40937C2-9BF7-4371-A64C-B44F5B6B895E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c9882e805504b2e3b2e4f4ebbe661268b2327a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046571"
---
# Get-AzureRemoteAppVM

## SYNOPSIS
Azure RemoteApp 컬렉션의 가상 컴퓨터를 가져옵니다.

## 구문과

```
Get-AzureRemoteAppVM -CollectionName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureRemoteAppVM** cmdlet은 세션 호스팅을 위해 Azure RemoteApp 컬렉션에서 만든 가상 컴퓨터를 가져옵니다.

## 예제의

### 예제 1: 컬렉션에 가상 컴퓨터 표시
```
PS C:\> Get-AzureRemoteAppVM -CollectionName "Contoso"
```

이 명령은 Contoso 라는 Azure RemoteApp 컬렉션에서 세션 호스팅에 사용 되는 가상 컴퓨터를 표시 합니다.

## 변수

### -CollectionName
Azure RemoteApp 컬렉션의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[다시 시작-AzureRemoteAppVM](./Restart-AzureRemoteAppVM.md)


