---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046579"
---
# Get-AzureRemoteAppTemplateImage

## SYNOPSIS
Azure RemoteApp 템플릿 이미지에 대 한 정보를 검색 합니다.

## 구문과

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureRemoteAppTemplateImage** Cmdlet은 Microsoft Azure의 Azure RemoteApp 템플릿 이미지에 대 한 정보를 검색 합니다.
이 cmdlet은 지정 된 템플릿 이미지에 대 한 정보를 포함 하는 개체를 반환 합니다.
서식 파일 이미지를 지정 하지 않으면 현재 구독에 있는 모든 템플릿 이미지에 대 한 정보를 검색 합니다.

## 예제의

### 예제 1: 모든 템플릿 이미지 목록 가져오기
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

이 명령은 모든 템플릿 이미지 목록을 반환 합니다.

### 예제 2: 지정 된 서식 파일 이미지에 대 한 정보 검색
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

이 명령은 ContosoApps 이라는 서식 파일 이미지에 대 한 정보를 검색 합니다.

## 변수

### -ImageName
Azure RemoteApp 템플릿 이미지의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[Get-AzureRemoteAppStartMenuProgram](./Get-AzureRemoteAppStartMenuProgram.md)


