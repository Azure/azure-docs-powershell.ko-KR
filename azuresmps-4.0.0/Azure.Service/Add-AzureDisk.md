---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 16A34F31-1C61-4911-8C1F-9F82683524A1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 775d2deff8a83e758d48fb9328bf4156b142d20c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046393"
---
# Add-AzureDisk

## SYNOPSIS
디스크를 Azure 디스크 리포지토리에 추가 합니다.

## 구문과

```
Add-AzureDisk [-DiskName] <String> [-MediaLocation] <String> [-Label <String>] [-OS <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## 설명은
**추가-AzureDisk** cmdlet는 현재 구독의 Azure 디스크 리포지토리에 디스크를 추가 합니다.
이 cmdlet은 시스템 디스크 또는 데이터 디스크를 추가할 수 있습니다.
시스템 디스크를 추가 하려면 *OS* 매개 변수를 사용 하 여 운영 체제 유형을 지정 합니다.

## 예제의

### 예제 1: Windows 운영 체제를 사용 하는 시동 디스크 추가
```
PS C:\> Add-AzureDisk -DiskName "MyWinDisk" -MediaLocation "http://contosostorage.blob.core.azure.com/vhds/winserver-system.vhd" -Label "StartupDisk" -OS "Windows"
```

이 명령은 디스크 리포지토리에 시스템 디스크를 추가 합니다.
시스템 디스크는 Windows 운영 체제를 사용 합니다.

### 예제 2: 데이터 디스크 추가
```
PS C:\> Add-AzureDisk -DiskName "MyDataDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/winserver-data.vhd" -Label "DataDisk"
```

이 명령은 데이터 디스크를 추가 합니다.

### 예제 3: Linux 시스템 디스크 추가
```
PS C:\> Add-AzureDisk -DiskName "MyLinuxDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/linuxsys.vhd" -OS "Linux"
```

이 명령은 Linux 시스템 디스크를 추가 합니다.

## 변수

### -DiskName
이 cmdlet이 추가 하는 디스크의 이름을 지정 합니다.

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

### -레이블
이 cmdlet이 추가 하는 디스크에 대 한 디스크 레이블을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MediaLocation
Azure Storage에서 디스크의 실제 위치를 지정 합니다.
이 값은 현재 구독 및 저장소 계정의 blob 페이지를 나타냅니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OS
시스템 디스크의 운영 체제 종류를 지정 합니다.
유효한 값은 다음과 같습니다. 

- 창을 
- Linux 

이 매개 변수를 지정 하지 않으면 cmdlet이 디스크를 데이터 디스크로 추가 합니다.

```yaml
Type: String
Parameter Sets: (All)
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

### DiskContext

## 상속자

## 관련 링크

[Get-AzureDisk](./Get-AzureDisk.md)

[-AzureDisk 제거](./Remove-AzureDisk.md)

[업데이트-AzureDisk](./Update-AzureDisk.md)


