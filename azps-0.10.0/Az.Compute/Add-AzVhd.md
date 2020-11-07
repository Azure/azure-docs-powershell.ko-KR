---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: 28d38fd88bada5b1c73557ea0d85bacf8ab2b6c0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877125"
---
# Add-AzVhd

## SYNOPSIS
온-프레미스 가상 컴퓨터의 가상 하드 디스크를 Azure의 클라우드 저장소 계정에 있는 blob로 업로드 합니다.

## 구문과

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzVhd** cmdlet은 온-프레미스 가상 하드 디스크를 .vhd 파일 형식으로 blob 저장소 계정에 고정 가상 하드 디스크로 업로드 합니다.
지정 된 대상 URI에서 사용 될 업 로더 스레드 수를 구성 하거나 기존 blob을 덮어쓸 수 있습니다.
또한 지원 되는 온-프레미스 .vhd 파일의 패치 된 버전을 업로드할 수 있습니다.
기본 가상 하드 디스크를 이미 업로드 한 경우 기본 이미지를 부모로 사용 하는 차이점 보관용 디스크를 업로드할 수 있습니다.
SA (공유 액세스 서명) URI도 지원 됩니다.

## 예제의

### 예제 1: VHD 파일 추가
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

이 명령은 저장소 계정에 .vhd 파일을 추가 합니다.

### 예제 2: VHD 파일 추가 및 대상 덮어쓰기
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

이 명령은 저장소 계정에 .vhd 파일을 추가 합니다.
명령이 기존 파일을 덮어씁니다.

### 예제 3: VHD 파일 추가 및 스레드 수 지정
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

이 명령은 저장소 계정에 .vhd 파일을 추가 합니다.
명령은 파일을 업로드 하는 데 사용할 스레드 수를 지정 합니다.

### 예제 4: VHD 파일 추가 및 SAS URI 지정
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

이 명령은 저장소 계정에 .vhd 파일을 추가 하 고 SAS URI를 지정 합니다.

## 변수

### -AsJob
백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.

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

### -BaseImageUriToPatch
Azure Blob Storage의 기본 이미지 blob에 대 한 URI를 지정 합니다.
이 매개 변수의 값으로 SA를 지정할 수 있습니다.

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -대상
Blob 저장소의 blob URI를 지정 합니다.
매개 변수는 SAS URI를 지원 하지만, 패치 시나리오는 대상에 SAS URI가 될 수 없습니다.

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

### -LocalFilePath
로컬 .vhd 파일의 경로를 지정 합니다.

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
.Vhd 파일을 업로드할 때 사용할 업 로더 스레드 수를 지정 합니다.

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
이 cmdlet이 지정 된 대상 URI (있는 경우)에서 기존 blob을 덮어쓴다는 것을 나타냅니다.

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

### -ResourceGroupName
가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### VhdUploadContext를 계산 합니다.

## 상속자

## 관련 링크

[저장-AzVhd](./Save-AzVhd.md)


