---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 75A50C59-28D1-4D29-A420-D24BF479F79E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29e5e7e0bc2fcc0ce93186cf966f18d6c9c3e372
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046157"
---
# Remove-AzureDisk

## SYNOPSIS
Azure 디스크 리포지토리에서 디스크를 제거 합니다.

## 구문과

```
Remove-AzureDisk [-DiskName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**제거-azuredisk** cmdlet는 현재 구독의 Azure 디스크 리포지토리에서 디스크를 제거 합니다.
기본적으로이 cmdlet은 blob 저장소에서 VHD (가상 하드 디스크) 파일을 삭제 하지 않습니다.
VHD를 삭제 하려면 *Deletevhd* 매개 변수를 지정 합니다.

## 예제의

### 예제 1: 디스크 제거
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk"
```

이 명령은 디스크 리포지토리에서 ContosoDataDisk disk 라는 디스크를 제거 합니다.
이 명령은 VHD를 삭제 하지 않습니다.

### 예제 2: 디스크 제거 및 삭제
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk" -DeleteVHD
```

이 명령은 디스크 리포지토리에서 ContosoDataDisk disk 라는 디스크를 제거 합니다.
이 명령은 DeleteVHD 매개 변수를 지정 합니다.
따라서 명령은 Azure 저장소에서 VHD를 삭제 합니다.

## 변수

### -DeleteVHD
이 cmdlet이 blob 저장소에서 VHD를 제거 함을 나타냅니다.

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

### -DiskName
이 cmdlet이 제거 하는 디스크 리포지토리에서 데이터 디스크의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

[Get-AzureDisk](./Get-AzureDisk.md)

[업데이트-AzureDisk](./Update-AzureDisk.md)


