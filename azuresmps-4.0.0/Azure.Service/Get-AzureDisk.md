---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046354"
---
# Get-AzureDisk

## SYNOPSIS
Azure 디스크 리포지토리의 디스크에 대 한 정보를 가져옵니다.

## 구문과

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**Get AzureDisk** cmdlet은 현재 구독에 대 한 Azure 디스크 리포지토리에 저장 된 디스크에 대 한 정보를 가져옵니다.
이 cmdlet은 리포지토리의 모든 디스크에 대 한 정보 목록을 반환 합니다.
특정 디스크에 대 한 정보를 보려면 디스크의 이름을 지정 합니다.

## 예제의

### 예제 1: 디스크에 대 한 정보 가져오기
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

이 명령은 디스크 리포지토리에서 ContosoDataDisk 이라는 디스크에 대 한 정보 데이터를 가져옵니다.

### 예제 2: 모든 디스크에 대 한 정보 가져오기
```
PS C:\> Get-AzureDisk
```

이 명령은 디스크 리포지토리의 모든 디스크에 대 한 정보를 가져옵니다.

### 예제 3: 디스크에 대 한 정보 가져오기
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

이 명령은 현재 가상 컴퓨터에 연결 되어 있지 않은 디스크 리포지토리의 모든 디스크에 대 한 데이터를 가져옵니다.
명령은 모든 디스크에 대 한 정보를 가져오고 각 개체를 **Where-object** cmdlet에 전달 합니다.
해당 cmdlet은 **AttachedTo** 속성에 대 한 $Null 값이 없는 모든 디스크를 삭제 합니다.
명령은 **Format 테이블** cmdlet을 사용 하 여 목록의 형식을 표로 지정 합니다.

## 변수

### -DiskName
이 cmdlet에 대 한 정보를 가져오는 디스크 리포지토리의 디스크 이름을 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[추가-AzureDisk](./Add-AzureDisk.md)

[-AzureDisk 제거](./Remove-AzureDisk.md)

[업데이트-AzureDisk](./Update-AzureDisk.md)


