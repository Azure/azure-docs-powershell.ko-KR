---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6B274EA-7FF2-46B0-8622-0DD17E9ADDD6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5531684de38a4a42aee4c131dbe58cd143370796
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046577"
---
# Get-AzureRemoteAppSession

## SYNOPSIS
컬렉션에 대 한 모든 활성 및 연결 되지 않은 Azure RemoteApp 세션을 나열 합니다.

## 구문과

```
Get-AzureRemoteAppSession [-CollectionName] <String> [[-UserUpn] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**AzureRemoteAppSession** Cmdlet은 azure remoteapp 컬렉션에 대 한 모든 활성 및 연결 되지 않은 azure RemoteApp 세션을 나열 합니다.

## 예제의

### 예제 1: 컬렉션의 모든 세션 나열
```
PS C:\> Get-AzureRemoteAppSession -CollectionName "ContosoApps"
```

이 명령은 ContosoApps 이라는 Azure RemoteApp 컬렉션의 모든 세션을 나열 합니다.

## 변수

### -CollectionName
Azure RemoteApp 컬렉션의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
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

### -UserUpn
Azure RemoteApp 세션을 가져올 사용자의 UPN (사용자 계정 이름)을 지정 합니다.
예를 들어 UPN은 다음 형식이 될 수 있습니다 PattiFuller@contoso.com .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[연결 해제-AzureRemoteAppSession](./Disconnect-AzureRemoteAppSession.md)

[AzureRemoteAppSessionLogoff-호출](./Invoke-AzureRemoteAppSessionLogoff.md)

[송신-AzureRemoteAppSessionMessage](./Send-AzureRemoteAppSessionMessage.md)


