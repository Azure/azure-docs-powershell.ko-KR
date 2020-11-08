---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 99DC239C-EA68-4830-9345-762CD6A3F68C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 320b95add2806f48121151a71bdf36a572fa05a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045718"
---
# Add-AzureVhd

## SYNOPSIS
온-프레미스 컴퓨터의 VHD 파일을 Azure의 클라우드 저장소 계정에 있는 blob에 업로드 합니다.

## 구문과

```
Add-AzureVhd [-Destination] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfUploaderThreads] <Int32>]
 [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
Vhd (가상 하드 디스크) 이미지에서 blob 저장소 계정에 대 한 **추가-azurevhd** cmdlet 업로드를 고정 된 .vhd 이미지로 변환할 수 있습니다.
이 파일에는 지정 된 대상 URI에 이미 존재 하는 blob을 사용 하거나 덮어쓰는 업 로더 스레드 수를 지정 하는 등 업로드 프로세스를 구성 하는 매개 변수가 있습니다.
온-프레미스 VHD 이미지의 경우 패치 시나리오가 지원 되므로 이미 업로드 한 기본 이미지를 업로드할 필요 없이 diff 디스크 이미지를 업로드할 수 있습니다. SA (공유 액세스 서명) URI도 지원 됩니다.

## 예제의

### 예제 1: VHD 파일 추가
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

이 명령은 저장소 계정에 .vhd 파일을 추가 합니다.

### 예제 2: VHD 파일 추가 및 대상 덮어쓰기
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

이 명령은 저장소 계정에 .vhd 파일을 추가 합니다.

### 예제 3: VHD 파일 추가 및 스레드 수 지정
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

이 명령은 저장소 계정에 .vhd 파일을 추가 하 고 파일을 업로드 하는 데 사용할 스레드 수를 지정 합니다.

### 예제 4: VHD 파일 추가 및 SAS URI 지정
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01-09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveOSIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

이 명령은 저장소 계정에 .vhd 파일을 추가 하 고 SAS URI를 지정 합니다.

## 변수

### -BaseImageUriToPatch
Azure Blob Storage의 기본 이미지 blob에 대 한 URI를 지정 합니다.
URI 입력의 SA도 지원 됩니다.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -대상
Microsoft Azure Blob 저장소의 blob에 대 한 URI를 지정 합니다.
URI 입력의 SA가 지원 됩니다.
그러나 패치 시나리오에서 대상은 SAS URI 일 수 없습니다.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
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

### -LocalFilePath
로컬 .vhd 파일의 파일 경로를 분류 합니다.

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberOfUploaderThreads
업로드에 사용할 스레드 수를 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OverWrite
이 cmdlet이 지정 된 대상 URI (있는 경우)의 기존 blob을 삭제 하도록 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
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

[-AzureVhd 저장](./Save-AzureVhd.md)


