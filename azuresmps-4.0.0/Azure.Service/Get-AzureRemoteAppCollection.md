---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046329"
---
# Get-AzureRemoteAppCollection

## SYNOPSIS
Azure RemoteApp 컬렉션에 대 한 정보를 검색 합니다.

## 구문과

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureRemoteAppCollection** Cmdlet은 Microsoft Azure의 Azure RemoteApp 컬렉션에 대 한 정보를 검색 합니다.
이 메서드는 특정 컬렉션에 대 한 정보를 포함 하는 개체를 반환 하 고, 지정 된 컬렉션이 없는 경우에는 현재 구독의 모든 컬렉션에 대해 제공 합니다.

## 예제의

### 예제 1: 모든 컬렉션 목록 가져오기
```
PS C:\> Get-AzureRemoteAppCollection
```

이 명령은 구독에 있는 모든 Azure RemoteApp 컬렉션 목록을 반환 합니다.

### 예제 2: 지정 된 컬렉션에 대 한 정보 가져오기
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

이 명령은 ContosoApps 이라는 Azure RemoteApp 컬렉션에 대 한 정보를 반환 합니다.

### 예제 3: 와일드 카드를 사용 하 여 컬렉션 목록 가져오기
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

이 명령은 모든 Azure RemoteApp 컬렉션 일치 재무 *의 목록을 반환 합니다.

## 변수

### -CollectionName
Azure RemoteApp 컬렉션의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
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

[새로운 AzureRemoteAppCollection](./New-AzureRemoteAppCollection.md)

[제거-AzureRemoteAppCollection](./Remove-AzureRemoteAppCollection.md)

[Set-AzureRemoteAppCollection](./Set-AzureRemoteAppCollection.md)

[업데이트-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


