---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045630"
---
# Get-AzureRemoteAppVmStaleAdObject

## SYNOPSIS
더 이상 존재 하지 않는 Azure RemoteApp 가상 컴퓨터와 연결 된 Azure Active Directory의 개체를 가져옵니다.

## 구문과

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureRemoteAppVmStaleAdObject** cmdlet은 더 이상 존재 하지 않는 azure RemoteApp 가상 컴퓨터와 연결 된 Azure Active Directory의 개체를 가져옵니다.
이 cmdlet은 가져오는 각 개체의 이름을 표시 합니다.

## 예제의

### 예제 1: 컬렉션에 대 한 부실 개체 가져오기
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

이 두 번째 명령은 Contoso 라는 컬렉션에 대 한 부실 개체를 가져옵니다.

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

### -Credential
이 작업을 수행할 수 있는 권한이 있는 자격 증명을 지정 합니다.
**PSCredential** 개체를 가져오려면 **Get-Credential** cmdlet을 사용 합니다.
이 매개 변수를 지정 하지 않으면이 cmdlet은 현재 사용자 자격 증명을 사용 합니다.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### 이름

## 상속자

## 관련 링크

[일반-AzureRemoteAppVmStaleAdObject](./Clear-AzureRemoteAppVmStaleAdObject.md)


