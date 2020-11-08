---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046570"
---
# Get-AzureRemoteAppVNet

## SYNOPSIS
Azure에서 Azure RemoteApp 가상 네트워크에 대 한 정보를 검색 합니다.

## 구문과

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**AzureRemoteAppVNet** Cmdlet은 Microsoft Azure에서 Azure RemoteApp 가상 네트워크에 대 한 정보를 검색 합니다.
이 cmdlet은 지정 된 가상 네트워크에 대 한 정보를 포함 하는 개체를 반환 합니다.
가상 네트워크를 지정 하지 않으면이 cmdlet은 현재 구독의 모든 가상 네트워크에 대 한 정보를 반환 합니다.

## 예제의

### 예제 1: 가상 네트워크에 대 한 정보 검색
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

이 명령은 ContosoVNet 이라는 가상 네트워크에 대 한 정보를 가져옵니다.

## 변수

### -IncludeSharedKey
이 cmdlet에 가상 네트워크에 대해 검색 하는 정보의 공유 키 값이 포함 되어 있음을 나타냅니다.

```yaml
Type: SwitchParameter
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

### -VNetName
Azure RemoteApp 가상 네트워크의 이름을 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Set-AzureRemoteAppVNet](./Set-AzureRemoteAppVNet.md)


