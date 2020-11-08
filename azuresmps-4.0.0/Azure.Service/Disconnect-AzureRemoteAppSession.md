---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 514C33F8-F0B8-4F37-AB2D-BB54DD754931
online version: ''
schema: 2.0.0
ms.openlocfilehash: c256ce8ba720eb08ffec2ab56ecca40ab74f4948
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045686"
---
# Disconnect-AzureRemoteAppSession

## SYNOPSIS
Azure RemoteApp 세션의 연결을 끊습니다.

## 구문과

```
Disconnect-AzureRemoteAppSession [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**AzureRemoteAppSession** cmdlet에서 사용자의 Azure RemoteApp 세션 연결을 끊습니다.
사용자의 클라이언트가 Azure RemoteApp 세션에서 연결을 끊고 사용자의 프로그램이 계속 실행 됩니다.

## 예제의

### 예제 1: 사용자 세션 연결 끊기
```
PS C:\> Disconnect-AzureRemoteAppSession -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com"
```

이 명령은 UPN이 있는 사용자의 ContosoApps 컬렉션에서 Azure RemoteApp 세션의 연결을 끊습니다 PattiFuller@contoso.com .

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
예를 들어 사용자의 UPN (사용자 계정 이름)을 지정 합니다 PattiFuller@contoso.com .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
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

[Get-AzureRemoteAppSession](./Get-AzureRemoteAppSession.md)

[AzureRemoteAppSessionLogoff-호출](./Invoke-AzureRemoteAppSessionLogoff.md)

[송신-AzureRemoteAppSessionMessage](./Send-AzureRemoteAppSessionMessage.md)


