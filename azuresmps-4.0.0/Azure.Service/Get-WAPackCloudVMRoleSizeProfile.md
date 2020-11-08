---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046508"
---
# Get-WAPackCloudVMRoleSizeProfile

## SYNOPSIS
클라우드 VM 역할 크기 프로필 개체를 가져옵니다.

## 구문과

### 비어 있음 (기본값)
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**WAPackCloudVMRoleSizeProfile** cmdlet은 가상 컴퓨터에 대 한 클라우드 VM 역할 크기 프로필 개체를 가져옵니다.

## 예제의

### 예제 1: 이름을 사용 하 여 클라우드 VM 역할 크기 프로필 가져오기
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

이 명령은 Small 이라는 크기 프로필을 가져옵니다.

### 예제 2: 모든 클라우드 VM 역할 크기 프로필 가져오기
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

이 명령은 모든 크기 프로필을 가져옵니다.

## 변수

### -이름
클라우드 VM 역할 크기 프로필의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: False
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

[Get-WAPackVM](./Get-WAPackVM.md)


